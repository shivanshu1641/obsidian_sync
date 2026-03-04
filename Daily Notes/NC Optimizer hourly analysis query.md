---
created: 2025-12-25T15:31
updated: 2026-03-04
tags:
  - DailyNote
topics:
  - "[[2026Q1]]"
type:
  - "[[Daily Note]]"
Status: TBD
Project:
---
```
WITH

spends AS (

SELECT

date(target_start_utc) AS target_date,

EXTRACT(hour FROM target_start_utc) AS target_hour,

REGEXP_REPLACE(

LOWER(REGEXP_EXTRACT(campaign, r'^([^-\n\r]*?)(?:-|$)')),

r'[^a-z]',

'') AS tld,

campaign,

sum(impressions) AS impressions,

sum(spend) AS spend

FROM `revved.vw_api_reports_hourly_downlaoded`

WHERE

(

lower(campaign) NOT LIKE "%target%"

OR lower(Campaign) NOT LIKE "%else 0 ends%")

GROUP BY ALL

),

domain_level_nr AS (

SELECT

date(nr.creation_date) AS creation_date,

EXTRACT(hour FROM nr.creation_date) AS creation_hour,

nr.tld,

nr.domain_id,

nr.net_revenue,

nr.period,

nr.promo_tag,

nr.domain,

p.first_renewal_prediction,

p.second_renewal_prediction,

p.subsequent_renewal_prediction,

p.npv,

p.projected_renew_arpt,

m.flag

FROM

(

SELECT *

FROM `radix_data.newreg`

WHERE

lower(client_shortname) = "namecheap"

AND date(Creation_date) >= "2025-01-01"

AND mbg = 0

AND promo_tag = "reg_price_promo"

) nr

LEFT JOIN `common_data.predictions` p

ON nr.domain_id = p.domain_id

LEFT JOIN `radixbi-249015.revved.nc_regs_mapping` m

ON nr.domain_id = m.domain_id

),

agg_nr AS (

SELECT

creation_date,

creation_hour,

tld,

period,

sum(CASE WHEN flag = "revved" THEN net_revenue ELSE 0 END)

AS revved_net_revenue,

COUNT(CASE WHEN flag = "revved" THEN domain_id END)

AS revved_domain_count,

sum(CASE WHEN flag = "revved" THEN first_renewal_prediction ELSE 0 END)

AS revved_first_renewal_prediction,

sum(CASE WHEN flag = "revved" THEN second_renewal_prediction ELSE 0 END)

AS revved_second_renewal_prediction,

sum(

CASE WHEN flag = "revved" THEN subsequent_renewal_prediction ELSE 0 END)

AS revved_subsequent_renewal_prediction,

sum(CASE WHEN flag = "revved" THEN npv ELSE 0 END) AS revved_npv,

sum(CASE WHEN flag = "revved" THEN projected_renew_arpt ELSE 0 END)

AS revved_projected_renew_arpt,

sum(CASE WHEN flag = "other" THEN net_revenue ELSE 0 END)

AS other_net_revenue,

COUNT(CASE WHEN flag = "other" THEN domain_id END)

AS other_domain_count,

sum(CASE WHEN flag = "other" THEN first_renewal_prediction ELSE 0 END)

AS other_first_renewal_prediction,

sum(CASE WHEN flag = "other" THEN second_renewal_prediction ELSE 0 END)

AS other_second_renewal_prediction,

sum(

CASE WHEN flag = "other" THEN subsequent_renewal_prediction ELSE 0 END)

AS other_subsequent_renewal_prediction,

sum(CASE WHEN flag = "other" THEN npv ELSE 0 END) AS other_npv,

sum(CASE WHEN flag = "other" THEN projected_renew_arpt ELSE 0 END)

AS other_projected_renew_arpt,

sum(CASE WHEN flag = "api" THEN net_revenue ELSE 0 END)

AS api_net_revenue,

COUNT(CASE WHEN flag = "api" THEN domain_id END)

AS api_domain_count,

sum(CASE WHEN flag = "api" THEN first_renewal_prediction ELSE 0 END)

AS api_first_renewal_prediction,

sum(CASE WHEN flag = "api" THEN second_renewal_prediction ELSE 0 END)

AS api_second_renewal_prediction,

sum(CASE WHEN flag = "api" THEN subsequent_renewal_prediction ELSE 0 END)

AS api_subsequent_renewal_prediction,

sum(CASE WHEN flag = "api" THEN npv ELSE 0 END) AS api_npv,

sum(CASE WHEN flag = "api" THEN projected_renew_arpt ELSE 0 END)

AS api_projected_renew_arpt

FROM domain_level_nr

GROUP BY ALL

)

SELECT * FROM agg_nr
```