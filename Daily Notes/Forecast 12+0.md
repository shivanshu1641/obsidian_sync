---
created: 2026-01-15
updated: 2026-02-07
tags:
  - Work/recurring
topics:
  - "[[2026Q1]]"
type:
  - "[[Daily Note]]"
Status: TBD
---
**Forecast Update Query**
```
CREATE OR REPLACE TABLE `radixbi-249015.npv_projection.forecast_std_12_0_2025`

AS

SELECT

CAST("forecast_12_0" AS STRING) AS forecast_cut,

"newreg" AS reg_type,

CAST(client_shortname AS STRING) AS client_shortname,

CAST(registrar_shortname AS STRING) AS registrar_shortname,

CAST(client_am AS STRING) AS client_am,

CAST(tld AS STRING) AS tld,

CAST(year AS FLOAT64) AS year,

CAST(month AS FLOAT64) AS month,

CAST(`type` AS STRING) AS type,

CAST(promo_tag AS STRING) AS promo_tag,

CAST(period AS FLOAT64) AS period,

CAST(domain_count AS FLOAT64) AS domain_count,

CAST(domain_year_count AS FLOAT64) AS domain_year_count,

CAST(reg_revenue AS FLOAT64) AS reg_revenue,

CAST(first_renewal_rate AS FLOAT64) AS first_renewal_rate,

CAST(second_renewal_rate AS FLOAT64) AS second_renewal_rate,

CAST(subsq_renewal_rate AS FLOAT64) AS subsequent_renewal_rate,

CAST(renew_arpt AS FLOAT64) AS renew_arpt,

CAST(npv AS FLOAT64) AS npv,

CAST(mdf AS FLOAT64) AS mdf,

CAST(net_npv AS FLOAT64) AS net_npv

FROM

`shiva_adhoc.forecast_std_12_0_2025`;

  

CREATE OR REPLACE TABLE `radixbi-249015.npv_projection.forecast_premium_12_0_2025`

AS

SELECT

CAST("forecast_12_0" AS STRING) AS forecast_cut,

"premium" AS reg_type,

CAST(client_shortname AS STRING) AS client_shortname,

CAST(registrar_shortname AS STRING) AS registrar_shortname,

CAST(client_am AS STRING) AS client_am,

CAST(tld AS STRING) AS tld,

CAST(year AS FLOAT64) AS year,

CAST(month AS FLOAT64) AS month,

CAST(`type` AS STRING) AS type,

CAST(promo_tag AS STRING) AS promo_tag,

CAST(period AS FLOAT64) AS period,

CAST(domain_count AS FLOAT64) AS domain_count,

CAST(domain_year_count AS FLOAT64) AS domain_year_count,

CAST(reg_revenue AS FLOAT64) AS reg_revenue,

CAST(first_renewal_rate AS FLOAT64) AS first_renewal_rate,

CAST(second_renewal_rate AS FLOAT64) AS second_renewal_rate,

CAST(subsq_renewal_rate AS FLOAT64) AS subsequent_renewal_rate,

CAST(renew_arpt AS FLOAT64) AS renew_arpt,

CAST(npv AS FLOAT64) AS npv,

CAST(mdf AS FLOAT64) AS mdf,

CAST(net_npv AS FLOAT64) AS net_npv

FROM

`shiva_adhoc.forecast_premium_12_0_2025`;
```

```
CREATE OR REPLACE TABLE `radixbi-249015.pnl_master.forecast_renew_12_0_2025`

AS

SELECT

timeline,

reg_type,

renewed_count,

tld,

registrar_shortname,

client_shortname,

expiry_month,

domain_count ,

renewal_revenue,

renewed_domain_years,

renewed_domain_count,

"forecast_12_0" AS forecast_cut

FROM

`radixbi-249015.shiva_adhoc.forecast_renew_12_0_2025`

WHERE reg_type = "renew"
```

```
CREATE OR REPLACE TABLE `radixbi-249015.pnl_master.forecast_premium_renew_12_0_2025`

AS

SELECT

timeline,

reg_type,

renewed_count,

tld,

registrar_shortname,

client_shortname,

expiry_month,

domain_count expiring_domain_count,

renewal_revenue,

renewed_domain_years,

renewed_domain_count,

"forecast_12_0" AS forecast_cut

FROM

`radixbi-249015.shiva_adhoc.forecast_renew_12_0_2025`

WHERE reg_type = "premium_renew"
```

```
CREATE OR REPLACE TABLE `radixbi-249015.pnl_master.forecast_premium_renew_12_0_2025`

AS

SELECT

timeline,

reg_type,

CASE

WHEN renewed_count = 1 THEN "premium_first_renews"

WHEN renewed_count = 2 THEN "premium_second_renews"

ELSE "premium_subsequent_renews"

END

AS renewal_type,

tld,

registrar_shortname,

client_shortname,

expiry_month,

domain_count expiring_domain_count,

renewal_revenue,

renewed_domain_years,

renewed_domain_count,

"forecast_12_0" AS forecast_cut

FROM

`radixbi-249015.shiva_adhoc.forecast_renew_12_0_2025`

WHERE reg_type = "premium_renew"
```

All Done