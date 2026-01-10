---
created: 2025-12-25T15:31
updated: 2026-01-09T18:16
tags:
  - Work/recurring
topics:
  - "[[2026Q1]]"
type:
  - "[[Daily Note]]"
Status: TBD
---
Forecast Update Query
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