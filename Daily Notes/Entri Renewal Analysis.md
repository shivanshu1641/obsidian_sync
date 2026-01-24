---
created: 2025-12-25T15:31
updated: 2026-01-23
tags:
  - DailyNote
  - work/Item
topics:
  - "[[2026Q1]]"
  - "[[Adhoc]]"
type:
  - "[[Daily Note]]"
Status: TBD
Project:
---
```
UPDATE `whoisdb.other_tld` AS t

SET client_shortname = LOWER(CONCAT('entri_', b.client_name))

FROM

(

SELECT domain, date(`date`) AS dt, client_name,

FROM `shiva_adhoc.temp_entri_all_tld_data`

GROUP BY ALL

) AS b

WHERE

t.domain = b.domain

AND abs(date_diff(DATE(b.dt), DATE(t.creation_date), day)) <= 3

AND date(t.creation_date) >= "2022-01-01"

AND lower(client_shortname) NOT LIKE "entri_%"

AND lower(registrar_shortname) = "1&1 internet"
```