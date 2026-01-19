---
created: 2025-12-25T15:31
updated: 2026-01-19T19:26
tags:
  - work/project
topics:
  - "[[2026Q1]]"
Project:
  - "[[Optimizer GD]]"
Status: TBD
---
**Bug in Autobidder** -- 2026-01-14
```
SELECT *

FROM `radixbi-249015.serp_godaddy_ads.bot_activity_log_vw`

WHERE date(created_at) = "2026-01-15" and type like "%optimizer%"
```
Autobidder not taking action basis the suggestions


