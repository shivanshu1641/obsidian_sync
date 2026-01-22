---
created: 2025-12-25T15:31
updated: 2026-01-22
tags:
  - work/project
topics:
  - "[[2026Q1]]"
Project:
  - "[[APM]]"
Status: TBD
---
- Pattern Detection
	- [ ] High Volume Handleling
- Proximity Score
	- [ ] Word based proximity 
- Gibb score
	- [ ] Entire - done / triggered for 2025
- E2E

```
WITH

long_newreg AS (

SELECT domain_id, date(transaction_date) AS creation_date

FROM `watchtower.new_registrations`

WHERE

date(transaction_date)

BETWEEN date_sub(current_date(), INTERVAL 180 day)

AND current_date()

),

curr_newreg AS (

SELECT *

FROM long_newreg

WHERE

date(Creation_date)

BETWEEN date_sub(current_date(), INTERVAL 15 day)

AND current_date()

),

mid_newreg AS (

SELECT *

FROM long_newreg

WHERE

date(Creation_date)

BETWEEN date_sub(current_date(), INTERVAL 30 day)

AND current_date()

),

proactive AS (

SELECT domain_id, 1 AS proactive

FROM `watchtower.domains_reported`

WHERE

domain_id NOT IN (

SELECT domain_id

FROM `watchtower.domains_unsuspended`

WHERE domain_id IS NOT NULL

)

AND domain_id IN (

SELECT domain_id FROM long_newreg WHERE domain_id IS NOT NULL

)

AND source_id = 17

),

reactive AS (

SELECT domain_id, 1 AS reactive

FROM `watchtower.domains_reported`

WHERE

domain_id NOT IN (

SELECT domain_id

FROM `watchtower.domains_unsuspended`

WHERE domain_id IS NOT NULL

)

AND domain_id IN (

SELECT domain_id FROM long_newreg WHERE domain_id IS NOT NULL

)

AND source_id <> 17

),

kw_data AS (

SELECT *

FROM `prepped_data.wordninja_split`

WHERE

date(creation_date)

BETWEEN date_sub(current_date(), INTERVAL 180 day)

AND current_date()

),

long_newreg_abuse AS (

WITH

raw AS (

SELECT

lnr.*,

coalesce(proactive, 0) AS proactive,

coalesce(reactive, 0) AS reactive,

word,

FROM long_newreg lnr

LEFT JOIN proactive p

ON lnr.domain_id = p.domain_id

LEFT JOIN reactive r

ON lnr.domain_id = r.domain_id

LEFT JOIN kw_data k

ON CAST(lnr.domain_id AS string) = k.domain_id

)

SELECT

word,

CASE

WHEN sum(proactive) > 100

THEN sum(proactive) / COUNT(domain_id)

ELSE 0

END AS plr,

sum(proactive) AS plc,

CASE

WHEN sum(reactive) > 100

THEN sum(reactive) / COUNT(domain_id)

ELSE 0

END AS rlr,

sum(reactive) AS rlc,

FROM raw

GROUP BY ALL

),

mid_newreg_abuse AS (

WITH

raw AS (

SELECT

mnr.*,

coalesce(proactive, 0) AS proactive,

coalesce(reactive, 0) AS reactive,

word,

FROM mid_newreg mnr

LEFT JOIN proactive p

ON mnr.domain_id = p.domain_id

LEFT JOIN reactive r

ON mnr.domain_id = r.domain_id

LEFT JOIN kw_data k

ON CAST(mnr.domain_id AS string) = k.domain_id

)

SELECT

word,

CASE

WHEN sum(proactive) > 20

THEN sum(proactive) / COUNT(domain_id)

ELSE 0

END AS pmr,

sum(proactive) AS pmc,

CASE

WHEN sum(reactive) > 20

THEN sum(reactive) / COUNT(domain_id)

ELSE 0

END AS rmr,

sum(reactive) AS rmc,

FROM raw

GROUP BY ALL

),

curr_newreg_exploded AS (

SELECT c_nr.*, coalesce(k.word,"") as word, pmr, pmc, rmr, rmc, plr, plc, rlr, rlc,

FROM curr_newreg c_nr

LEFT JOIN kw_data k

ON CAST(c_nr.domain_id AS string) = k.domain_id

LEFT JOIN long_newreg_abuse lna

ON k.word = lna.word

LEFT JOIN mid_newreg_abuse mna

ON k.word = mna.word

)

SELECT

min(creation_date) AS creation_date,

domain_id,

array_agg(word) AS words,

sum(pmr) pmr,

sum(pmc) pmc,

sum(rmr) rmr,

sum(rmc) rmc,

sum(plr) plr,

sum(plc) plc,

sum(rlr) rlr,

sum(rlc) rlc,

FROM curr_newreg_exploded

GROUP BY domain_id
```



	- Pattern Bulk done
	- gibb done
	- proxim
		- word based logic pending - removed this is a seperate component now done
		- check rust logic done
	- word based logic done
	- brand done

historic runs
- brand match done
- prox done
- gibb score in done
- word ninja in done
- word prox done
- pattern in progress