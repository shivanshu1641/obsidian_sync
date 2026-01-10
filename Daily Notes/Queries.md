---
created: 2025-12-25T15:31
updated: 2026-01-10T12:01
tags:
  - work
topics:
  - "[[2026Q1]]"
type:
Status: TBD
---
### Content

**Bluehost store query**

```
SELECT

(CASE

WHEN sld NOT IN ( SELECT REPLACE(domain, CONCAT(".",tld),"") AS sld FROM `cnic_dump.dumdata_bq`) THEN 1

ELSE 0

END

) is_dot_store_available,

*

FROM

`radixbi-249015.storeleads.sl_new_data_mapped`

WHERE

end_month = "202507"

AND LOWER(registrar_shortname) LIKE "%bluehost%"

AND sld_parts = 1

AND tld != "store"

```

**Bigcartel store queries**
```
SELECT

CASE

WHEN end_month = "202507" THEN "live"

ELSE "store_not_active"

END

AS store_flag,

*

FROM

`radixbi-249015.storeleads.sl_new_data_mapped`

WHERE

platform = "bigcartel"

AND end_month = "202507"

AND tld = "store"

AND LOWER(client_shortname) LIKE "%dotserve%"
```

**GD Purchase Premium Query**
```
SELECT

*

FROM

`radixbi-249015.godaddy_data.rtb_purchase_dump`

WHERE

domain_name IN (

SELECT

domain

FROM

`radix_data.premium_newreg`)
```

**Storeleads category null data**
```
SELECT

name,

platform,

client_shortname,

created_at,

categories

FROM

`radixbi-249015.storeleads.sl_new_data_mapped_all_cols`

WHERE

end_month = "202508"

AND platform = "shopify"

AND ARRAY_LENGTH(categories) = 0

AND tld = "com"

AND sld_parts = 1

AND client_shortname IS NOT NULL

ORDER BY

created_at DESC

LIMIT

10000
```

**Namestore premium searches**
```
WITH

D AS (

WITH

-- ----------------------------------------

-- Filtered registry data (whois + newreg)

-- ----------------------------------------

-- ----------------------------------------

-- Store search log with utm_campaign only

-- ----------------------------------------

store_searches AS (

WITH

split_query AS (

SELECT

unique_id,

url,

SPLIT(SPLIT(url, '?')[

OFFSET

(1)], '&') AS param_pairs

FROM

`radixbi-249015.elevate.store_search_log`

WHERE

url IS NOT NULL

AND STRPOS(url, '?') > 0 ),

key_value_pairs AS (

SELECT

unique_id,

url,

SPLIT(pair, '=')[

OFFSET

(0)] AS KEY,

SPLIT(pair, '=')[SAFE_OFFSET(1)] AS value

FROM

split_query,

UNNEST(param_pairs) AS pair ),

campaign_values AS (

SELECT

unique_id,

url,

MAX(

IF

(KEY = 'utm_campaign', value, NULL)) AS utm_campaign,

MAX(

IF

(KEY = 'pk_campaign', value, NULL)) AS pk_campaign

FROM

key_value_pairs

GROUP BY

unique_id,

url )

SELECT

s.id,

s.term,

s.url,

s.unique_id,

s.country,

s.created_date,

COALESCE(c.utm_campaign, c.pk_campaign) AS utm_campaign

FROM

`radixbi-249015.elevate.store_search_log` s

LEFT JOIN

campaign_values c

ON

s.unique_id = c.unique_id

AND s.url = c.url ),

-- ----------------------------------------

-- Online data with utm_campaign only

-- ----------------------------------------

online_data AS (

SELECT

"online" AS base,

id,

term,

url,

unique_id,

country,

created_date,

utmcampaign AS utm_campaign,

FROM

`elevate.online_search_log` ),

-- ----------------------------------------

-- Store data aligned to same schema

-- ----------------------------------------

store_data AS (

SELECT

"store" AS base,

s.id,

s.term,

s.url,

s.unique_id,

s.country,

s.created_date,

s.utm_campaign,

FROM

store_searches s )

-- ----------------------------------------

-- Final combined result

-- ----------------------------------------

SELECT

*

FROM

online_data

UNION ALL

SELECT

*

FROM

store_data)

SELECT

base,

COUNT(DISTINCT term) AS all_domain_search,

COUNT(DISTINCT

CASE

WHEN term IN ( SELECT domain FROM premium_db.premium_inventory) THEN term

END

) AS premium_domain_search,

COUNT(DISTINCT

CASE

WHEN REPLACE(term,CONCAT(".",base),"") IN ( SELECT sld FROM premium_db.premium_inventory) THEN term

END

) AS premium_sld_search,

FROM

d

GROUP BY

all
```


Storeleads query for shop bulk cr adds
```
SELECT

-- distinct name

reg_domain,

tld,

min_asof_date AS first_seen,

max_asof_date AS last_seen,

created_at_min,

CASE

WHEN end_month = "202510" THEN 1

ELSE 0

END

AS live,

CASE

WHEN abuse.domain is not null THEN 1

ELSE 0

END

AS abuse,

abuse.source as src

FROM

`radixbi-249015.storeleads.sl_new_data_mapped` sl

left join (select domain, `source` from `radixbi-249015.shiva_adhoc.other_tld_abuse_data` group by all qualify row_number() over(partition by domain)=1) as abuse

on sl.reg_domain = abuse.domain

WHERE

sld_parts = 1

AND created_at_min = "2024-11-15"

AND start_month != "202411"

-- AND tld = "shop"
```



```
Query for NPV Variation across months

WITH

filtered_archive_logs AS (

SELECT

archive_date,

date(date_trunc(archive_date, quarter)) AS archive_quarter,

date_sub(

date_trunc(

date_sub(archive_date, INTERVAL 2 month),

year),

INTERVAL 1 day) AS max_permissable_date

FROM `radixbi-249015.npv_data.npv_transaction_data_archive_logs`

WHERE lower(message) LIKE "%monthly%"

),

permissable_date_for_kpi AS (

SELECT *,

FROM filtered_archive_logs

QUALIFY

(row_number() OVER (PARTITION BY archive_quarter ORDER BY archive_date))

= 1

)

SELECT

date(date_trunc(Creation_date, year)) AS creation_year,

date(npv_vw.archive_date) AS archive_date,

reg_type,

sum(npv) AS npv,

sum(first_renewed_count) AS first_renewed_count,

FROM `radixbi-249015.npv_data.npv_transaction_data_archive` npv_vw

JOIN permissable_date_for_kpi p

ON

npv_vw.archive_date = p.archive_date

AND p.max_permissable_date >= npv_vw.creation_date

GROUP BY ALL

ORDER BY 1, 2

```