---
created: 2025-12-25T15:31
updated: 2026-01-20
tags:
  - work/Item
  - Work/recurring
topics:
  - "[[2026Q1]]"
type:
Status: TBD
---
```
  
  

UPDATE `ntld_renewals.gd_geo_level_preds_test_1` a

SET a.new_segmented_pred = b.new_segmented_pred

FROM `ntld_renewals.gd_geo_level_preds_test_tech` b

WHERE

a.tld = "tech"

AND DATE(a.creation_date) >= "2025-01-01"

AND a.geo NOT IN ("in", "cn")

AND a.reg_period = "1"

AND a.domain = b.domain

AND b.tld = "tech"

AND DATE(b.creation_date) >= "2025-01-01"

AND b.reg_period = 1;

  
  
  

UPDATE

`radixbi-249015.ntld_renewals.gd_geo_level_preds_test_1`

SET

new_segmented_pred = 0.4

WHERE

tld = "store"

AND geo = "ca"

and promo_tag = "domain_bundle_click_to_add_paid";

  

update `radixbi-249015.ntld_renewals.gd_geo_level_preds_test_1`

  

set new_segmented_pred = new_segmented_pred*1.99

where tld = "store"

and reg_period = '2' and promo_tag = "reg_price_promo"

and round(reg_revenue) = 12;

UPDATE `ntld_renewals.nc_cust_level_preds_test` a

SET a.new_segmented_pred = b.new_segmented_pred

FROM `ntld_renewals.nc_cust_level_preds_space` b

WHERE

a.tld = "space"

AND DATE(a.creation_date) >= "2024-12-01"

-- AND a.reg_revenue = 0.3

AND a.reg_period = "1"

AND a.domain = b.domain and a.domain_id = b.domain_id

AND b.tld = "space"

AND DATE(b.creation_date) >= "2024-12-01"

AND b.reg_period = "1";

  
  
  

UPDATE `ntld_renewals.nc_cust_level_preds_test` a

SET a.new_segmented_pred = b.new_segmented_pred

FROM `ntld_renewals.nc_cust_level_preds_tech` b

WHERE

a.tld = "tech"

AND DATE(a.creation_date) >= "2024-12-10"

AND a.reg_period = "1"

AND a.domain = b.domain and a.domain_id = b.domain_id

AND b.tld = "tech"

AND a.promo_tag = "reg_price_promo"

AND DATE(b.creation_date) >= "2024-12-10"

AND b.reg_period = 1;

  
  
  

UPDATE `ntld_renewals.nc_cust_level_preds_test` a

SET a.new_segmented_pred = b.new_segmented_pred

FROM `radixbi-249015.ntld_renewals.nc_cust_level_preds_fun` b

WHERE

a.tld = "fun"

AND DATE(a.creation_date) >= "2024-01-01"

AND a.reg_period = "1"

AND a.domain = b.domain

AND a.domain_id = b.domain_id

AND b.tld = "fun"

AND DATE(b.creation_date) >= "2024-01-01"

AND b.reg_period = 1;

  
  

UPDATE `ntld_renewals.nc_cust_level_preds_test` a

SET a.new_segmented_pred = b.new_segmented_pred

FROM `radixbi-249015.ntld_renewals.nc_cust_level_preds_site` b

WHERE

a.tld = "site"

AND DATE(a.creation_date) >= "2024-01-01"

AND a.reg_period = "1"

AND a.domain = b.domain

AND a.domain_id = b.domain_id

AND b.tld = "site"

AND DATE(b.creation_date) >= "2024-01-01"

AND b.reg_period = "1";

  
  

UPDATE

ntld_renewals.nc_cust_level_preds_test

SET

new_segmented_pred = 0.18

WHERE

tld = "fun"

AND DATE(Creation_date) >= "2025-01-01"

AND reg_period = "1"

AND reg_revenue = 5.98;

  
  

UPDATE

ntld_renewals.nc_cust_level_preds_test

SET

new_segmented_pred = 0.2

WHERE

tld = "fun"

AND DATE(Creation_date) >= "2025-01-01"

AND reg_period = "1"

AND reg_revenue = 7.8;

  
  
  
  
  

UPDATE

`ntld_renewals.nc_cust_level_preds_test`

SET

new_segmented_pred = 0.14

WHERE

tld = "fun"

AND ROUND(reg_revenue,2) = 3.18

AND DATE(creation_date) >= "2025-06-01"

AND reg_period = "1";

  

UPDATE

`ntld_renewals.gd_geo_level_preds_test_1`

SET

new_segmented_pred = 0.277

WHERE

tld = "fun"

AND ROUND(reg_revenue,2) = 1.5

AND DATE(creation_date) >= "2025-06-01"

AND reg_period = "1";

  
  
  

UPDATE

`ntld_renewals.gd_geo_level_preds_test_1`

SET

new_segmented_pred = 0.3

WHERE

tld = "fun"

AND ROUND(reg_revenue,2) = 2

AND DATE(creation_date) >= "2025-06-01"

AND reg_period = "1";

  

update

`ntld_renewals.gd_geo_level_preds_test_1`

set new_segmented_pred = case when new_segmented_pred *1.42 > 0.9 then 0.9 else new_segmented_pred *1.42 end

WHERE

tld = "store"

AND reg_period = "2"

AND reg_revenue = 25

AND DATE(creation_date) >= "2025-07-01";

  

update

`ntld_renewals.gd_geo_level_preds_test_1`

set new_segmented_pred = case when new_segmented_pred *1.42 > 0.9 then 0.9 else new_segmented_pred *1.42 end

WHERE

tld = "store"

AND reg_period = "2"

AND reg_revenue = 15

AND DATE(creation_date) >= "2025-07-01";

  
  
  

update

`ntld_renewals.gd_geo_level_preds_test_1`

set new_segmented_pred = case when new_segmented_pred *1.42 > 0.9 then 0.9 else new_segmented_pred *1.42 end

WHERE

tld = "store"

AND reg_period = "2"

AND reg_revenue = 25

AND DATE(creation_date) >= "2025-07-01";

  
  
  

update

`ntld_renewals.gd_geo_level_preds_test_1`

set new_segmented_pred = 0.35

WHERE

tld = "online"

AND reg_period = "2"

AND reg_revenue = 10

AND DATE(creation_date) >= "2025-07-01";

  
  

update

`ntld_renewals.gd_geo_level_preds_test_1`

set new_segmented_pred = 0.275

WHERE

tld = "online"

AND reg_period = "2"

AND reg_revenue = 5

AND DATE(creation_date) >= "2025-07-01";

  

update

`ntld_renewals.gd_geo_level_preds_test_1`

set new_segmented_pred = 0.02

WHERE

tld = "online"

AND reg_period = "1"

AND geo = "de"

AND DATE(creation_date) >= "2025-07-01";

  

update

`ntld_renewals.gd_geo_level_preds_test_1`

set new_segmented_pred = 0.55

WHERE

tld = "tech"

AND reg_period = "2"

AND reg_revenue = 22.5

AND DATE(creation_date) >= "2025-07-01";

  
  
  
  
  
  

-- UPDATE `ntld_renewals.gd_geo_level_preds_test_1`

-- set new_segmented_pred = new_segmented_pred*1.84

-- where tld = "store" and date(creation_date) >= "2025-10-01" and lower(geo_train) = "us" and reg_period = "1";

  
  

-- UPDATE `ntld_renewals.gd_geo_level_preds_test_1`

-- set new_segmented_pred = new_segmented_pred*1.33

-- where tld = "store" and date(creation_date) >= "2025-10-01" and lower(geo_train) <> "us" and reg_period = "1";

  
  
  
  

DELETE

FROM

`radixbi-249015.ntld_renewals.gd_geo_level_preds`

WHERE

1=1;

INSERT INTO

`radixbi-249015.ntld_renewals.gd_geo_level_preds` (

SELECT

domain_id, creation_date, client_shortname, tld, domain, reg_period, reg_revenue, geo, promo_tag, gibb_score_adv_prob, pattern_domain_count_updated, serp_flag, date, hour, hour_slab, sld_type, sld_length, app_share, geo_train, hour_domain, new_segmented_pred

FROM

`radixbi-249015.ntld_renewals.gd_geo_level_preds_test_1`);

DELETE

FROM

`radixbi-249015.ntld_renewals.nc_cust_level_preds`

WHERE

1=1;

INSERT INTO

`radixbi-249015.ntld_renewals.nc_cust_level_preds` (

SELECT

domain_id, creation_date, client_shortname, tld, domain, reg_period, reg_revenue, gibb_score_adv_prob, pattern_domain_count_updated, cust_per_domain, promo_tag, date, hour, hour_slab, sld_type, sld_length, app_share, hour_domain, new_segmented_pred

FROM

`radixbi-249015.ntld_renewals.nc_cust_level_preds_test`);
```