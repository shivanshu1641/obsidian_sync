---
created: 2025-12-25T15:31
updated: 2026-01-15T13:47
tags:
  - work/Item
topics:
  - "[[2026Q1]]"
Project:
  - "[[Adhoc]]"
Status: TBD
---
Query for dashboard

```
--- Query for NPV Variation

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