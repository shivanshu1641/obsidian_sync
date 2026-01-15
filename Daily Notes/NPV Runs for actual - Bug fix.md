---
created: 2025-12-25T15:31
updated: 2026-01-15T13:47
tags:
  - Work/bug
topics:
  - "[[2026Q1]]"
Project:
  - "[[Bug]]"
Status: In Progress
---
**Cloud Function Query**

```
CREATE OR REPLACE TABLE radixbi-249015.npv_data.dotserve_substitute_domains AS

SELECT domain_id, 
        0.3025 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        25 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        24.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        24.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-05-01" AND "2022-05-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        24.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        24.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        24.42 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-08-01" AND "2022-08-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        24 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        20.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        0.299 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        20 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        19.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        0.03 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        15 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "startupleague_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.03 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        15 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "startupleague_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.2869 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        14 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.228 as first_renew_pred, 
        0.608 as second_renew_pred, 
        0.745 as subsequent_renew_pred, 
        13.33 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotfun_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        12.5 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        10.55 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-08-01" AND "2022-08-31" UNION ALL 
SELECT domain_id, 
        1 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.5 as subsequent_renew_pred, 
        10 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        0.1868 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        10 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        10 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        10 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        10 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        10 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        10 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        10 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        9.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        9.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        9.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        9.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        9.54 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        9.26 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-05-01" AND "2022-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        9.25 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        9.23 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        9.22 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-07-01" AND "2022-07-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        9 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        8.39 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-08-01" AND "2022-08-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        8.33 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        8.33 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-05-01" AND "2022-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        8.2 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        7.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        7.77 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        7.49 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-08-01" AND "2022-08-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        6.66 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-12-01" AND "2022-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        5.58 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-12-01" AND "2022-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        4.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotpress_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        4.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotpress_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        4.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotpress_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-08-01" AND "2022-08-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        4.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotpress_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        4.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotpress_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        4.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotpress_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        4.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotpress_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.55 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        4.99 as new_reg_price, 
        49 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotpress_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        3.13 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.76 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        0.228 as first_renew_pred, 
        0.608 as second_renew_pred, 
        0.745 as subsequent_renew_pred, 
        2.67 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotfun_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        2.52 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        0.2168 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        2.35 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        0.22 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        2.07 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        2 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        2 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        2 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        2 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        2 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        2 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        1.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-07-01" AND "2022-07-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        1.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        1.99 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        1.81 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        0.168 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        1.71 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        1.63 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        1.59 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        0.0515 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        1.3 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        0.1144 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        1.19 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        1.16 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-05-01" AND "2022-05-31" UNION ALL 
SELECT domain_id, 
        0.228 as first_renew_pred, 
        0.608 as second_renew_pred, 
        0.745 as subsequent_renew_pred, 
        1.14 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotfun_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        1.11 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        1.09 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.1008 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        1.02 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.86 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.88 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        0.228 as first_renew_pred, 
        0.608 as second_renew_pred, 
        0.745 as subsequent_renew_pred, 
        1 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotfun_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        1 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        1 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        1 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        1 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        1 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        1 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        1 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        1 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        1 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.3323 as first_renew_pred, 
        0.6591 as second_renew_pred, 
        0.8225 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotfun_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.45 as second_renew_pred, 
        0.7 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "autods_dotserve inc"
        AND DATE(creation_date) BETWEEN "2025-01-08" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "ecombrands_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.05 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "ecombrands_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.45 as second_renew_pred, 
        0.7 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "autods_dotserve inc"
        AND DATE(creation_date) BETWEEN "2025-01-07" AND "2025-01-07" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.45 as second_renew_pred, 
        0.7 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "autods_dotserve inc"
        AND DATE(creation_date) BETWEEN "2025-01-01" AND "2025-01-06" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.45 as second_renew_pred, 
        0.7 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "autods_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.45 as second_renew_pred, 
        0.7 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "buildyourstore.ai_dotserve inc"
        AND DATE(creation_date) BETWEEN "2025-01-09" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.45 as second_renew_pred, 
        0.7 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "buildyourstore.ai_dotserve inc"
        AND DATE(creation_date) BETWEEN "2025-01-07" AND "2025-01-08" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.45 as second_renew_pred, 
        0.7 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "buildyourstore.ai_dotserve inc"
        AND DATE(creation_date) BETWEEN "2025-01-01" AND "2025-01-06" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.45 as second_renew_pred, 
        0.7 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "buildyourstore.ai_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-12-26" AND "2024-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.45 as second_renew_pred, 
        0.7 as subsequent_renew_pred, 
        0.99 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "buildyourstore.ai_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-12-25" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        1.01 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        1.01 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-05-01" AND "2022-05-31" UNION ALL 
SELECT domain_id, 
        0.0997 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0.89 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.83 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.46 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-07-01" AND "2022-07-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        3.1 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-08-01" AND "2022-08-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-05-01" AND "2022-05-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-07-01" AND "2022-07-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-08-01" AND "2022-08-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-12-01" AND "2022-12-31" UNION ALL 
SELECT domain_id, 
        1 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        0.2869 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.2999 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        1 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.5 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        0.1868 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.1728 as first_renew_pred, 
        0.6088 as second_renew_pred, 
        0.8254 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.1458 as first_renew_pred, 
        0.5997 as second_renew_pred, 
        0.8228 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.1482 as first_renew_pred, 
        0.5956 as second_renew_pred, 
        0.8194 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.1474 as first_renew_pred, 
        0.5934 as second_renew_pred, 
        0.8168 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-12-01" AND "2022-12-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        0.2998 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-08-01" AND "2022-08-31" UNION ALL 
SELECT domain_id, 
        0.1455 as first_renew_pred, 
        0.6063 as second_renew_pred, 
        0.8246 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-07-01" AND "2022-07-31" UNION ALL 
SELECT domain_id, 
        0.1641 as first_renew_pred, 
        0.6003 as second_renew_pred, 
        0.815 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        0.1454 as first_renew_pred, 
        0.601 as second_renew_pred, 
        0.8202 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.1971 as first_renew_pred, 
        0.6101 as second_renew_pred, 
        0.8191 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0.8 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.1219 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0.79 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.79 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-05-01" AND "2022-05-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.64 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.75 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-07-01" AND "2022-07-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0.73 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.0999 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0.71 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.0998 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0.67 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.65 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.5 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0.6 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.5 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.38 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        0.0999 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0.5 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0.5 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0.5 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.42 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-12-01" AND "2022-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.48 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        0.0012 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0.26 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        0.0247 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0.21 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.0282 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0.21 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0.37 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        0.0281 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0.33 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.0999 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0.36 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.0283 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0.22 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0.33 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.2196 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0.33 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.0288 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0.21 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0.32 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.0284 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0.36 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.22 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0.31 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.0286 as first_renew_pred, 
        0.392 as second_renew_pred, 
        0.626 as subsequent_renew_pred, 
        0.23 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.0285 as first_renew_pred, 
        0.392 as second_renew_pred, 
        0.626 as subsequent_renew_pred, 
        0.31 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.0285 as first_renew_pred, 
        0.392 as second_renew_pred, 
        0.626 as subsequent_renew_pred, 
        0.32 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.0288 as first_renew_pred, 
        0.392 as second_renew_pred, 
        0.626 as subsequent_renew_pred, 
        0.22 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.0286 as first_renew_pred, 
        0.392 as second_renew_pred, 
        0.626 as subsequent_renew_pred, 
        0.26 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.03 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.03 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0.48 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.03 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0.98 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.12 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0.19 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.204 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.76 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotfun_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.204 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.76 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotfun_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.228 as first_renew_pred, 
        0.608 as second_renew_pred, 
        0.745 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotfun_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.314 as first_renew_pred, 
        0.6575 as second_renew_pred, 
        0.8225 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotfun_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.3161 as first_renew_pred, 
        0.6493 as second_renew_pred, 
        0.8165 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotfun_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        0.1167 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        0.1105 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.1156 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.12 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.12 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.12 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.114 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.12 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.12 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.112 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.12 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.2947 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.292 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.3194 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-05-01" AND "2022-05-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-07-01" AND "2022-07-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.292 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-08-01" AND "2022-08-31" UNION ALL 
SELECT domain_id, 
        0.2944 as first_renew_pred, 
        0.6343 as second_renew_pred, 
        0.8125 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.1412 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.1175 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-07-01" AND "2022-07-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "uno"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        15 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "uno"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-12-01" AND "2022-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-12-01" AND "2022-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        15 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "pw"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        15 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "pw"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.25 as first_renew_pred, 
        0.6 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        0.25 as first_renew_pred, 
        0.6 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.25 as first_renew_pred, 
        0.6 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        0.0566 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        0.22 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2196 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.0997 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.0998 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.0998 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-12-01" AND "2022-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        0.3025 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2024-09-15" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.2211 as first_renew_pred, 
        0.6084 as second_renew_pred, 
        0.75422 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.155 as first_renew_pred, 
        0.498 as second_renew_pred, 
        0.656 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "uno"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.0515 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        0.168 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.2168 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        0.22 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.22 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2196 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.0997 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.0998 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.099 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.099 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.099 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.1868 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.3194 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.25 as first_renew_pred, 
        0.6 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.25 as first_renew_pred, 
        0.6 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.25 as first_renew_pred, 
        0.6 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.2007 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.1144 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.204 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.76 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.204 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.76 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        1 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.76 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-01-01" AND "2023-01-31" UNION ALL 
SELECT domain_id, 
        0.204 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.76 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.204 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.76 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.204 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.76 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.228 as first_renew_pred, 
        0.608 as second_renew_pred, 
        0.745 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.228 as first_renew_pred, 
        0.608 as second_renew_pred, 
        0.745 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.228 as first_renew_pred, 
        0.608 as second_renew_pred, 
        0.745 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.209 as first_renew_pred, 
        0.608 as second_renew_pred, 
        0.745 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.228 as first_renew_pred, 
        0.608 as second_renew_pred, 
        0.745 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.6575 as second_renew_pred, 
        0.8224 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.6493 as second_renew_pred, 
        0.8164 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.6591 as second_renew_pred, 
        0.8224 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.1008 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.1105 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.2054 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.2054 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.2091 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.2091 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.2062 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.21 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2998 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.2981 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.2984 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.2996 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.25 as second_renew_pred, 
        0.499 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.22 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.22 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2196 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.0997 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.0998 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.0987 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-02-01" AND "2023-02-28" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-03-01" AND "2023-03-31" UNION ALL 
SELECT domain_id, 
        0.0281 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.0283 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.198 as first_renew_pred, 
        0.574 as second_renew_pred, 
        0.704 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-04-01" AND "2023-04-30" UNION ALL 
SELECT domain_id, 
        0.2202 as first_renew_pred, 
        0.6268 as second_renew_pred, 
        0.7657 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-05-01" AND "2023-05-31" UNION ALL 
SELECT domain_id, 
        0.2244 as first_renew_pred, 
        0.6132 as second_renew_pred, 
        0.7595 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.2211 as first_renew_pred, 
        0.6084 as second_renew_pred, 
        0.7542 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.2432 as first_renew_pred, 
        0.5998 as second_renew_pred, 
        0.7357 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        0.2378 as first_renew_pred, 
        0.6102 as second_renew_pred, 
        0.7584 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.2531 as first_renew_pred, 
        0.6164 as second_renew_pred, 
        0.762 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.2516 as first_renew_pred, 
        0.616 as second_renew_pred, 
        0.7617 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        0.2079 as first_renew_pred, 
        0.594 as second_renew_pred, 
        0.7493 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.6343 as second_renew_pred, 
        0.8125 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.6257 as second_renew_pred, 
        0.8065 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.6375 as second_renew_pred, 
        0.8134 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-11-01" AND "2022-11-30" UNION ALL 
SELECT domain_id, 
        0.05 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-09-15" AND "2024-10-09" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.2057 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.0288 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        0.005 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-10-10" AND "2024-10-12" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        15 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "uno"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        0.2096 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-10-01" AND "2022-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        0.0288 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-06-01" AND "2023-06-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-09-01" AND "2022-09-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-08-01" AND "2022-08-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-08-01" AND "2022-08-31" UNION ALL 
SELECT domain_id, 
        0.0284 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.05 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-10-13" AND "2024-10-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-07-01" AND "2022-07-31" UNION ALL 
SELECT domain_id, 
        0.0284 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.629 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2023-07-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-07-01" AND "2022-07-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.0286 as first_renew_pred, 
        0.392 as second_renew_pred, 
        0.626 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-06-01" AND "2022-06-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-05-01" AND "2022-05-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-08-01" AND "2023-08-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-05-01" AND "2022-05-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.0282 as first_renew_pred, 
        0.392 as second_renew_pred, 
        0.626 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-09-01" AND "2023-09-30" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-04-01" AND "2022-04-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        0.029 as first_renew_pred, 
        0.392 as second_renew_pred, 
        0.626 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-10-01" AND "2023-10-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "dotonline_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.029 as first_renew_pred, 
        0.392 as second_renew_pred, 
        0.626 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-11-01" AND "2023-11-30" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "uno"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "press"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        0.0284 as first_renew_pred, 
        0.392 as second_renew_pred, 
        0.626 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-12-01" AND "2023-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.03 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0.98 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dottech_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-03-01" AND "2022-03-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.03 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-02-01" AND "2022-02-28" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "dotsite_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2022-01-01" AND "2022-01-31" UNION ALL 
SELECT domain_id, 
        0.05 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2024-01-31" UNION ALL 
SELECT domain_id, 
        0.05 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-02-01" AND "2024-02-29" UNION ALL 
SELECT domain_id, 
        0.05 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.31 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.76 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotfun_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.12 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.651 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dothost_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.03 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        15 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "uno"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2023-07-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotspace_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.03 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.1 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "fourthwall_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-01-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.6 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "events_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.65 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "fun"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2024-03-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.65 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "website"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.65 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "linklab_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.09 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.3 as first_renew_pred, 
        0.3 as second_renew_pred, 
        0.55 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.6 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        25 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.05 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2024-10-09" UNION ALL 
SELECT domain_id, 
        0.01 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "teamlinkstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        50 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "host"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        20 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-03-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.03 as first_renew_pred, 
        0.4 as second_renew_pred, 
        0.63 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2024-11-26" UNION ALL 
SELECT domain_id, 
        0.08 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-11-01" AND "2024-12-26" UNION ALL 
SELECT domain_id, 
        0 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-10-11" AND "2024-10-11" UNION ALL 
SELECT domain_id, 
        0.05 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "storedomains_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-10-12" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.03 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "tech"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-11-27" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.2 as first_renew_pred, 
        0.62 as second_renew_pred, 
        0.78 as subsequent_renew_pred, 
        0 as new_reg_price, 
        0 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "startwithstore_dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-04-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.04 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.77 as subsequent_renew_pred, 
        0 as new_reg_price, 
        40 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dotserve inc"
        AND DATE(creation_date) BETWEEN "2024-12-27" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        null as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "online"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2013-01-01" AND "2021-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        null as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "space"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2013-01-01" AND "2022-12-31" UNION ALL 
SELECT domain_id, 
        null as first_renew_pred, 
        null as second_renew_pred, 
        null as subsequent_renew_pred, 
        null as new_reg_price, 
        1.5 as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "site"
        AND LOWER(client_shortname) = "medianet_dotserve inc"
        AND DATE(creation_date) BETWEEN "2013-01-01" AND "2022-12-31" UNION ALL 
SELECT domain_id, 
        0.06 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.65 as subsequent_renew_pred, 
        null as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "debutify_store_dotserve inc"
        AND DATE(creation_date) BETWEEN "2025-01-01" AND "2025-12-31" UNION ALL 
SELECT domain_id, 
        0.115 as first_renew_pred, 
        0.5 as second_renew_pred, 
        0.7 as subsequent_renew_pred, 
        null as new_reg_price, 
        null as new_revenue 
        FROM radix_data.newreg WHERE
        mbg = 0
        AND tld = "store"
        AND LOWER(client_shortname) = "dropmagic_dotserve inc"
        AND DATE(creation_date) BETWEEN "2025-01-01" AND "2025-12-31";


        UPDATE
        npv_data.newreg_predictions_non_dp_20251229 a
        SET
            a.renew_prediction = COALESCE(b.first_renew_pred, a.renew_prediction),
            a.arpt = COALESCE(b.new_revenue, a.arpt),
            a.revenue = COALESCE(b.new_revenue, a.revenue),
            a.techops_cost = 
              CASE  WHEN (COALESCE(b.new_revenue, a.revenue) * 0.2) > 0.45 THEN 0.495
                    WHEN (COALESCE(b.new_revenue, a.revenue) * 0.2) <= 0.45 THEN (COALESCE(b.new_revenue, a.revenue) * 0.2) + 0.045
                END
        FROM (
            SELECT
            *
            FROM
            npv_data.dotserve_substitute_domains
            GROUP BY
            1,
            2,
            3,
            4,
            5,
            6) b
        WHERE
            a.domain_id = b.domain_id
            AND a.renewed_count = 1
            AND a.renewed = 0
            AND (
                b.first_renew_pred IS NOT NULL 
                OR b.new_revenue IS NOT NULL
            )
            AND (DATE(creation_date) BETWEEN "2013-01-01"
                AND "2025-12-31");


        UPDATE
        npv_data.newreg_predictions_non_dp_20251229 a
        SET
            a.renew_prediction = COALESCE(b.second_renew_pred, a.renew_prediction),
            a.arpt = COALESCE(b.new_revenue, a.arpt),
            a.revenue = COALESCE(b.new_revenue, a.revenue),
            a.techops_cost = 
              CASE  WHEN (COALESCE(b.new_revenue, a.revenue) * 0.2) > 0.45 THEN 0.495
                    WHEN (COALESCE(b.new_revenue, a.revenue) * 0.2) <= 0.45 THEN (COALESCE(b.new_revenue, a.revenue) * 0.2) + 0.045
                END
            FROM (
            SELECT
                *
            FROM
                npv_data.dotserve_substitute_domains
            GROUP BY
                1,
                2,
                3,
                4,
                5,
                6) b
            WHERE
            a.domain_id = b.domain_id
            AND a.renewed_count = 2
            AND a.renewed = 0
            AND (
                b.second_renew_pred IS NOT NULL 
                OR b.new_revenue IS NOT NULL
            )
            AND (DATE(creation_date) BETWEEN "2013-01-01"
                AND "2025-12-31");


        UPDATE
        npv_data.newreg_predictions_non_dp_20251229 a
        SET
            a.renew_prediction = COALESCE(b.subsequent_renew_pred, a.renew_prediction),
            a.arpt = COALESCE(b.new_revenue, a.arpt),
            a.revenue = COALESCE(b.new_revenue, a.revenue),
            a.techops_cost = 
              CASE  WHEN (COALESCE(b.new_revenue, a.revenue) * 0.2) > 0.45 THEN 0.495
                    WHEN (COALESCE(b.new_revenue, a.revenue) * 0.2) <= 0.45 THEN (COALESCE(b.new_revenue, a.revenue) * 0.2) + 0.045
                END
            FROM (
            SELECT
                *
            FROM
                npv_data.dotserve_substitute_domains
            GROUP BY
                1,
                2,
                3,
                4,
                5,
                7) b
            WHERE
            a.domain_id = b.domain_id
            AND a.renewed_count > 2
            AND a.renewed = 0
            AND (
                b.subsequent_renew_pred IS NOT NULL 
                OR b.new_revenue IS NOT NULL
            )
            AND (DATE(creation_date) BETWEEN "2013-01-01"
                AND "2025-12-31");


        UPDATE
        npv_data.newreg_predictions_non_dp_20251229 a
        SET
            a.arpt = COALESCE(ROUND(a.period * b.new_reg_price, 4), a.arpt),
            a.techops_cost = 
              CASE  WHEN (a.revenue * 0.2) > 0.45 THEN 0.495
                    WHEN (a.revenue * 0.2) <= 0.45 THEN (a.revenue * 0.2) + 0.045
                END
            FROM (
            SELECT
                *
            FROM
                npv_data.dotserve_substitute_domains
            GROUP BY
                1,
                2,
                3,
                4,
                5,
                8) b
            WHERE
            a.domain_id = b.domain_id
            AND a.renewed_count = 0
            AND b.new_reg_price IS NOT NULL
            AND (DATE(creation_date) BETWEEN "2013-01-01"
                AND "2025-12-31");



    CREATE OR REPLACE TABLE
      npv_data.substitute_domains AS
    SELECT
      domain_id,
      ROUND(MIN(new_segmented_pred), 4) AS first_renewal_prediction
    FROM
      radixbi-249015.ntld_renewals.gd_geo_level_preds
    WHERE
      (DATE(creation_date) BETWEEN "2022-01-01"
        AND "2025-12-31")
    GROUP BY
      1
    UNION ALL
    SELECT
      domain_id,
      ROUND(MIN(new_segmented_pred), 4) AS first_renewal_prediction
    FROM
      radixbi-249015.ntld_renewals.nc_cust_level_preds
    WHERE
      (DATE(creation_date) BETWEEN "2022-01-01"
        AND "2025-12-31")
    GROUP BY
      1;
  

  -- Create a temporary table that had all the domain ids for domain with specific rule
  CREATE OR REPLACE TABLE
    npv_data.godaddy_domains_with_rule AS
  

     -- Control Panel bundle for store at 30% Jan 2024 onwards
  SELECT
    domain_id,
    0.3 AS first_renewal_prediction
  FROM
    radixbi-249015.radix_data.newreg
  WHERE
    date(creation_date) >= "2024-01-01"
    and lower(client_shortname) = "go daddy"
    AND tld = "store"
    AND promo_tag = "control_panel_upsell"
    AND mbg = 0


     -- Control Panel bundle for Online at 35% Jan 2024 onwards
  UNION ALL
  SELECT
    domain_id,
    0.35 AS first_renewal_prediction
  FROM
    radixbi-249015.radix_data.newreg
  WHERE
    date(creation_date) >= "2024-01-01"
    and lower(client_shortname) = "go daddy"
    AND tld = "online"
    AND promo_tag = "control_panel_upsell"
    AND mbg = 0


    
  -- Adjustment rule for (GoDaddy, site, Sept 2024 starting => 7.3%)
  UNION ALL
  SELECT
    domain_id,
    0.04 AS first_renewal_prediction
  FROM
    radix_data.newreg
  WHERE
    date(creation_date) >= "2025-12-01"
    and lower(client_shortname) = "go daddy"
    AND tld IN ("site")
    AND promo_tag = "reg_price_promo"
    AND net_revenue <= 1.5
    AND mbg = 0

  -- Adjustment rule for (GoDaddy, online, Sept 2024 starting => 11%)
  UNION ALL
  SELECT
    domain_id,
    0.11 AS first_renewal_prediction
  FROM
    radix_data.newreg
  WHERE
    date(creation_date) >= "2025-12-01"
    and lower(client_shortname) = "go daddy"
    AND tld IN ("online")
    AND promo_tag = "reg_price_promo"
    AND mbg = 0
-- store 18% application
  UNION ALL
  SELECT
    domain_id,
    0.2 AS first_renewal_prediction
  FROM
    radix_data.newreg
  WHERE
    date(creation_date) >= "2025-12-01"
    and lower(client_shortname) = "go daddy"
    AND tld IN ("store")
    AND promo_tag = "reg_price_promo"
    AND mbg = 0


  -- Adjustment rule for (GoDaddy, space, Sept 2024 starting => 14.55%)
  UNION ALL
  SELECT
    domain_id,
    0.1455 AS first_renewal_prediction
  FROM
    radix_data.newreg
  WHERE
    date(creation_date) >= "2025-12-01"
    and lower(client_shortname) = "go daddy"
    AND tld IN ("space")
    AND promo_tag = "reg_price_promo"
    AND net_revenue <= 1.5
    AND mbg = 0

  -- Adjustment rule for (Namecheap, site, June 2024 starting => 1.95%)
  UNION ALL
  SELECT
    domain_id,
    0.05 AS first_renewal_prediction
  FROM
    radix_data.newreg
  WHERE
    date(creation_date) >= "2025-12-01"
    and lower(client_shortname) = "namecheap"
    AND tld IN ("site")
    AND promo_tag = "reg_price_promo"
    AND net_revenue <= 3
    AND mbg = 0

  -- Adjustment rule for (Namecheap, store, June 2024 starting => 6.2%)
  UNION ALL
  SELECT
    domain_id,
    0.062 AS first_renewal_prediction
  FROM
    radix_data.newreg
  WHERE
    date(creation_date) >= "2025-12-01"
    and lower(client_shortname) = "namecheap"
    AND tld IN ("store")
    AND promo_tag = "reg_price_promo"
    AND net_revenue = 0.3
    AND mbg = 0

  -- Adjustment rule for (Namecheap, online, June 2024 starting => 10%)
  UNION ALL
  SELECT
    domain_id,
    0.1 AS first_renewal_prediction
  FROM
    radix_data.newreg
  WHERE
    date(creation_date) >= "2025-12-01"
    and lower(client_shortname) = "namecheap"
    AND tld IN ("online")
    AND promo_tag = "reg_price_promo"
    AND net_revenue = 0.3
    AND mbg = 0;


  -- Update those domain ids so that it has latest renew percentage
  UPDATE
    npv_data.substitute_domains a
  SET
    first_renewal_prediction = d.first_renewal_prediction
  FROM
    npv_data.godaddy_domains_with_rule d
  where a.domain_id = d.domain_id;

  INSERT INTO
    npv_data.substitute_domains
  SELECT
    *
  FROM
    npv_data.godaddy_domains_with_rule
  WHERE
    domain_id NOT IN (
    SELECT
      domain_id
    FROM
      npv_data.substitute_domains
    GROUP BY
      1);
  

      INSERT INTO
        npv_data.substitute_domains
      SELECT
        domain_id,
        0.0 AS first_renewal_prediction
      FROM
        radix_data.newreg
      WHERE
        mbg = 0
        AND (domain_id IN (
          SELECT
            domain_id
          FROM
            radixbi-249015.watchtower.domains_suspended
          WHERE
            domain_id NOT IN (
            SELECT
              domain_id
            FROM
              radixbi-249015.watchtower.domains_unsuspended)))
        AND (DATE(creation_date) BETWEEN "2013-01-01" and "2025-12-31")
      GROUP BY
        1;
  

      UPDATE
        npv_data.newreg_predictions_non_dp_20251229 a
      SET
        renew_prediction = first_renewal_prediction
      FROM (
        SELECT
          domain_id,
          MIN(first_renewal_prediction) first_renewal_prediction
        FROM
          npv_data.substitute_domains
        GROUP BY
          1) d
      WHERE
        a.domain_id = d.domain_id
        AND a.renewed_count = 1
        AND a.renewed = 0
        AND (DATE(creation_date) BETWEEN "2013-01-01"
          AND "2025-12-31");
  

    CREATE OR REPLACE TABLE
    npv_data.sensitivity_substitute AS
  

      -- Sensitivity for third renewal
      SELECT
        x.domain_id,
        x.percentage,
        x.price,
        y.renewed_count
      FROM (
        SELECT
          domain_id,
          0.97 AS percentage,
          25 AS price
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND ((tld IN ("fun")
              AND DATE(creation_date) BETWEEN "2020-08-01"
              AND "2021-07-31")
            OR (tld IN ("site")
              AND DATE(creation_date) BETWEEN "2020-08-01"
              AND "2021-07-31"))) x
      LEFT JOIN (
        SELECT
          *
        FROM
          UNNEST(GENERATE_ARRAY(3, (
              SELECT
                MAX(renewed_count) AS renewed_count
              FROM
                npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y
      ON
        TRUE
      UNION ALL
      SELECT
        x.domain_id,
        x.percentage,
        x.price,
        y.renewed_count
      FROM (
        SELECT
          domain_id,
          0.97 AS percentage,
          20 AS price
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND ((tld IN ("space")
              AND DATE(creation_date) BETWEEN "2020-08-01"
              AND "2021-07-31")
            OR (tld IN ("website")
              AND DATE(creation_date) BETWEEN "2020-08-01"
              AND "2021-07-31"))) x
      LEFT JOIN (
        SELECT
          *
        FROM
          UNNEST(GENERATE_ARRAY(3, (
              SELECT
                MAX(renewed_count) AS renewed_count
              FROM
                npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y
      ON
        TRUE
  

      UNION ALL
      
      -- Sensitivity for second renewal
      SELECT
        domain_id,
        0.9 AS percentage,
        25 AS price,
        2 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND (tld IN ("fun")
          AND DATE(creation_date) BETWEEN "2021-08-01"
          AND "2022-07-31")
      UNION ALL
      SELECT
        domain_id,
        0.95 AS percentage,
        25 AS price,
        2 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND (tld IN ("site")
          AND DATE(creation_date) BETWEEN "2021-08-01"
          AND "2022-07-31")
      UNION ALL
      SELECT
        domain_id,
        0.95 AS percentage,
        20 AS price,
        2 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND ((tld IN ("space")
            AND DATE(creation_date) BETWEEN "2021-08-01"
          AND "2022-07-31")
          OR (tld IN ("website")
            AND DATE(creation_date) BETWEEN "2021-08-01"
          AND "2022-07-31"))
      UNION ALL
      SELECT
        domain_id,
        0.97 AS percentage,
        40 AS price,
        2 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND (tld IN ("tech")
          AND DATE(creation_date) BETWEEN "2021-08-01"
          AND "2022-07-31")
  
    

      UNION ALL
      
      -- Sensitivity for first renewal before august 2023
      SELECT
        domain_id,
        0.85 AS percentage,
        25 AS price,
        1 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND ((tld IN ("fun")
            AND DATE(creation_date) BETWEEN "2022-08-01"
            AND "2023-07-31")
          OR (tld IN ("site")
            AND DATE(creation_date) BETWEEN "2022-08-01"
            AND "2023-07-31"))
      UNION ALL
      SELECT
        domain_id,
        0.9 AS percentage,
        20 AS price,
        1 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND ((tld IN ("space")
            AND DATE(creation_date) BETWEEN "2022-08-01"
            AND "2023-07-31")
          OR (tld IN ("website")
            AND DATE(creation_date) BETWEEN "2022-08-01"
            AND "2023-07-31"))
      UNION ALL
      SELECT
        domain_id,
        0.95 AS percentage,
        40 AS price,
        1 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND (tld IN ("tech")
          AND DATE(creation_date) BETWEEN "2022-08-01"
            AND "2023-07-31")
  
    

      UNION ALL
      
      -- Sensitivity for first renewal for and after august 2023
      SELECT
        domain_id,
        0.95 AS percentage,
        25 AS price,
        1 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND ((tld IN ("fun")
            AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31")
          OR (tld IN ("site")
            AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31"))
      UNION ALL
      SELECT
        domain_id,
        0.95 AS percentage,
        20 AS price,
        1 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND ((tld IN ("space")
            AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31")
          OR (tld IN ("website")
            AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31"))
      UNION ALL
      SELECT
        domain_id,
        0.98 AS percentage,
        40 AS price,
        1 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND (tld IN ("tech")
          AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31")
      UNION ALL


      ------------------------------------------------------------------------------------------------------------------------------------
        -- Sensitivity for second renewal
      SELECT
        domain_id,
        0.98 AS percentage,
        25 AS price,
        2 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND ((tld IN ("fun")
            AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31")
          OR (tld IN ("site")
            AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31"))
      UNION ALL
      SELECT
        domain_id,
        0.98 AS percentage,
        20 AS price,
        2 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND ((tld IN ("space")
            AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31")
          OR (tld IN ("website")
            AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31"))
      UNION ALL
      SELECT
        domain_id,
        0.98 AS percentage,
        40 AS price,
        2 AS renewed_count
      FROM
        radixbi-249015.radix_data.newreg
      WHERE
        (mbg = 0)
        AND (tld IN ("tech")
          AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31")
      UNION ALL


      ------------------------------------------------------------------------------------------------------------------------------------
        -- Sensitivity for third renewal
      SELECT
        x.domain_id,
        x.percentage,
        x.price,
        y.renewed_count
      FROM (
        SELECT
          domain_id,
          0.98 AS percentage,
          25 AS price
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND ((tld IN ("fun")
              AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31")
            OR (tld IN ("site")
              AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31"))) x
      LEFT JOIN (
        SELECT
          *
        FROM
          UNNEST(GENERATE_ARRAY(3, (
              SELECT
                MAX(renewed_count) AS renewed_count
              FROM
                npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y
      ON
        TRUE
      UNION ALL
      SELECT
        x.domain_id,
        x.percentage,
        x.price,
        y.renewed_count
      FROM (
        SELECT
          domain_id,
          0.98 AS percentage,
          20 AS price
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND ((tld IN ("space")
              AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31")
            OR (tld IN ("website")
              AND DATE(creation_date) BETWEEN "2023-08-01" AND "2024-12-31"))) x
      LEFT JOIN (
        SELECT
          *
        FROM
          UNNEST(GENERATE_ARRAY(3, (
              SELECT
                MAX(renewed_count) AS renewed_count
              FROM
                npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y
      ON
        TRUE
  
    

 UNION ALL 
 
        SELECT
          domain_id,
          0.95 AS percentage,
          49 AS price,
          1 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("press")
            AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-14")
        UNION ALL
        SELECT
          domain_id,
          0.95 AS percentage,
          65 AS price,
          1 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("host")
            AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-14")
        UNION ALL
        SELECT
          domain_id,
          0.95 AS percentage,
          45 AS price,
          1 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("tech")
            AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-14")
    
 UNION ALL 
 
        SELECT
          domain_id,
          0.97 AS percentage,
          49 AS price,
          1 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("press")
            AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15")
        UNION ALL
        SELECT
          domain_id,
          0.97 AS percentage,
          65 AS price,
          1 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("host")
            AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15")
        UNION ALL
        SELECT
          domain_id,
          0.97 AS percentage,
          45 AS price,
          1 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("tech")
            AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15")
    

 UNION ALL 
 
        SELECT
          domain_id,
          0.98 AS percentage,
          49 AS price,
          2 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("press")
            AND DATE(creation_date) BETWEEN "2022-01-15" AND "2023-01-14")
        UNION ALL
        SELECT
          domain_id,
          0.98 AS percentage,
          65 AS price,
          2 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("host")
            AND DATE(creation_date) BETWEEN "2022-01-15" AND "2023-01-14")
        UNION ALL
        SELECT
          domain_id,
          0.98 AS percentage,
          45 AS price,
          2 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("tech")
            AND DATE(creation_date) BETWEEN "2022-01-15" AND "2023-01-14")
    
 UNION ALL 
 
        SELECT
          domain_id,
          0.98 AS percentage,
          49 AS price,
          2 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("press")
            AND DATE(creation_date) BETWEEN "2023-01-15" AND "2025-01-15")
        UNION ALL
        SELECT
          domain_id,
          0.98 AS percentage,
          65 AS price,
          2 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("host")
            AND DATE(creation_date) BETWEEN "2023-01-15" AND "2025-01-15")
        UNION ALL
        SELECT
          domain_id,
          0.98 AS percentage,
          45 AS price,
          2 AS renewed_count
        FROM
          radixbi-249015.radix_data.newreg
        WHERE
          (mbg = 0)
          AND (tld IN ("tech")
            AND DATE(creation_date) BETWEEN "2023-01-15" AND "2025-01-15")
    

 UNION ALL 

      -- First renewal (old sensitivity, new price)
      SELECT domain_id, 0.90 AS percentage, 30.0 AS price, 1 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "fun"    AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.95 AS percentage, 25.0 AS price, 1 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "space"  AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.95 AS percentage, 27.5 AS price, 1 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "online" AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.90 AS percentage, 27.5 AS price, 1 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "site"   AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.90 AS percentage, 17.5 AS price, 1 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "pw"     AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.85 AS percentage, 20.0 AS price, 1 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "uno"    AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.95 AS percentage, 42.0 AS price, 1 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "store"  AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.95 AS percentage, 62.0 AS price, 1 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "press"  AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.95 AS percentage, 79.0 AS price, 1 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "host"   AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.95 AS percentage, 49.0 AS price, 1 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "tech"   AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    

 UNION ALL 

      -- Second renewal (old sensitivity, new price)
      SELECT domain_id, 0.95 AS percentage, 30.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "fun"    AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      UNION ALL
      SELECT domain_id, 0.97 AS percentage, 25.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "space"  AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      UNION ALL
      SELECT domain_id, 0.97 AS percentage, 27.5 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "online" AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      UNION ALL
      SELECT domain_id, 0.95 AS percentage, 27.5 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "site"   AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      UNION ALL
      SELECT domain_id, 0.90 AS percentage, 17.5 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "pw"     AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      UNION ALL
      SELECT domain_id, 0.90 AS percentage, 20.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "uno"    AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      UNION ALL
      SELECT domain_id, 0.97 AS percentage, 42.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "store"  AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      UNION ALL
      SELECT domain_id, 0.97 AS percentage, 62.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "press"  AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      UNION ALL
      SELECT domain_id, 0.97 AS percentage, 79.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "host"   AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      UNION ALL
      SELECT domain_id, 0.97 AS percentage, 49.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "tech"   AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
 UNION ALL 

      -- Second renewal (new sensitivity, new price)
      SELECT domain_id, 0.97 AS percentage, 30.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "fun"    AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.99 AS percentage, 25.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "space"  AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.99 AS percentage, 27.5 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "online" AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.97 AS percentage, 27.5 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "site"   AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.92 AS percentage, 17.5 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "pw"     AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.92 AS percentage, 20.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "uno"    AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.99 AS percentage, 42.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "store"  AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.99 AS percentage, 62.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "press"  AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.99 AS percentage, 79.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "host"   AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
      UNION ALL
      SELECT domain_id, 0.99 AS percentage, 49.0 AS price, 2 AS renewed_count FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "tech"   AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    

 UNION ALL 

      -- Subseq renewal (old sensitivity, new price, renewed_count >= 3)
      SELECT x.domain_id, 0.95 AS percentage, 30.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "fun"    AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.97 AS percentage, 25.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "space"  AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.97 AS percentage, 27.5 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "online" AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.95 AS percentage, 27.5 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "site"   AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.90 AS percentage, 17.5 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "pw"     AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.90 AS percentage, 20.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "uno"    AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.97 AS percentage, 42.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "store"  AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.97 AS percentage, 62.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "press"  AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.97 AS percentage, 79.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "host"   AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 1.00 AS percentage, 49.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "tech"   AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
    
 UNION ALL 

      -- Subseq renewal (new sensitivity, new price, renewed_count >= 3)
      SELECT x.domain_id, 0.97 AS percentage, 30.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "fun"    AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.99 AS percentage, 25.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "space"  AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.99 AS percentage, 27.5 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "online" AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.97 AS percentage, 27.5 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "site"   AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.92 AS percentage, 17.5 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "pw"     AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.92 AS percentage, 20.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "uno"    AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.99 AS percentage, 42.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "store"  AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.99 AS percentage, 62.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "press"  AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 0.99 AS percentage, 79.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "host"   AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
      UNION ALL
      SELECT x.domain_id, 1.00 AS percentage, 49.0 AS price, y.renewed_count FROM (SELECT domain_id FROM radixbi-249015.radix_data.newreg WHERE mbg = 0 AND tld = "tech"   AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15") x LEFT JOIN (SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) AS renewed_count FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count) y ON TRUE
    
UNION ALL

      SELECT domain_id, 0.9 AS percentage, 13 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "space"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.9 AS percentage, 14 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "online"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.9 AS percentage, 14 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "site"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.9 AS percentage, 13 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "website"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.9 AS percentage, 14 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "pw"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.9 AS percentage, 13 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "uno"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.8 AS percentage, 16 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "store"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.8 AS percentage, 30 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "tech"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.8 AS percentage, 25 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "fun"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.5 AS percentage, 30 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "press"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.5 AS percentage, 30 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "host"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 13 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "space"
        AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 14 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "online"
        AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 14 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "site"
        AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 13 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "website"
        AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 14 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "pw"
        AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 13 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "uno"
        AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 16 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "store"
        AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 30 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "tech"
        AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 25 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "fun"
        AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
UNION ALL

      SELECT domain_id, 0.7 AS percentage, 30 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "press"
        AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
UNION ALL

      SELECT domain_id, 0.7 AS percentage, 30 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "host"
        AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
    
UNION ALL

      SELECT x.domain_id, 0.95 AS percentage, 13 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "space"
          AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.95 AS percentage, 14 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "online"
          AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.95 AS percentage, 14 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "site"
          AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.95 AS percentage, 13 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "website"
          AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.95 AS percentage, 14 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "pw"
          AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.95 AS percentage, 13 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "uno"
          AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.95 AS percentage, 16 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "store"
          AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.95 AS percentage, 30 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "tech"
          AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.95 AS percentage, 25 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "fun"
          AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.7 AS percentage, 30 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "press"
          AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.7 AS percentage, 30 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "host"
          AND DATE(creation_date) BETWEEN "2023-01-15" AND "2024-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    

UNION ALL

      SELECT domain_id, 0.975 AS percentage, 13 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "space"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.975 AS percentage, 14 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "online"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.975 AS percentage, 14 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "site"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.975 AS percentage, 13 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "website"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.975 AS percentage, 14 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "pw"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.975 AS percentage, 13 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "uno"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.975 AS percentage, 16 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "store"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.975 AS percentage, 30 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "tech"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.975 AS percentage, 25 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "fun"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.85 AS percentage, 30 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "press"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT domain_id, 0.85 AS percentage, 30 AS price, 2 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_country) = "china"
        AND tld = "host"
        AND DATE(creation_date) BETWEEN "2025-01-15" AND "2025-12-31"
    
UNION ALL

      SELECT x.domain_id, 0.975 AS percentage, 13 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "space"
          AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.975 AS percentage, 14 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "online"
          AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.975 AS percentage, 14 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "site"
          AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.975 AS percentage, 13 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "website"
          AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.975 AS percentage, 14 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "pw"
          AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.975 AS percentage, 13 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "uno"
          AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.975 AS percentage, 16 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "store"
          AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.975 AS percentage, 30 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "tech"
          AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.975 AS percentage, 25 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "fun"
          AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.85 AS percentage, 30 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "press"
          AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT x.domain_id, 0.85 AS percentage, 30 AS price, y.renewed_count
      FROM (
        SELECT domain_id
        FROM radixbi-249015.radix_data.newreg
        WHERE mbg = 0
          AND LOWER(client_country) = "china"
          AND tld = "host"
          AND DATE(creation_date) BETWEEN "2024-01-15" AND "2025-01-15"
      ) x
      LEFT JOIN (
        SELECT * FROM UNNEST(GENERATE_ARRAY(3, (SELECT MAX(renewed_count) FROM npv_data.newreg_predictions_non_dp_20251229) + 3)) AS renewed_count
      ) y
      ON TRUE
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 23 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "online"
        AND DATE(creation_date) BETWEEN "2024-12-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 21 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "site"
        AND DATE(creation_date) BETWEEN "2024-12-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.9 AS percentage, 13 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "website"
        AND DATE(creation_date) BETWEEN "2024-12-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 21 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "space"
        AND DATE(creation_date) BETWEEN "2024-12-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 22 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "fun"
        AND DATE(creation_date) BETWEEN "2024-12-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 12.5 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "pw"
        AND DATE(creation_date) BETWEEN "2024-12-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 40 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "tech"
        AND DATE(creation_date) BETWEEN "2024-12-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 30.5 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "store"
        AND DATE(creation_date) BETWEEN "2024-12-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 29 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "press"
        AND DATE(creation_date) BETWEEN "2024-12-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 32 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "host"
        AND DATE(creation_date) BETWEEN "2024-12-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 24 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "online"
        AND DATE(creation_date) BETWEEN "2025-06-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 22 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "site"
        AND DATE(creation_date) BETWEEN "2025-06-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.9 AS percentage, 14 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "website"
        AND DATE(creation_date) BETWEEN "2025-06-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 22 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "space"
        AND DATE(creation_date) BETWEEN "2025-06-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 24 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "fun"
        AND DATE(creation_date) BETWEEN "2025-06-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 13.5 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "pw"
        AND DATE(creation_date) BETWEEN "2025-06-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 42 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "tech"
        AND DATE(creation_date) BETWEEN "2025-06-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.95 AS percentage, 31.5 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "store"
        AND DATE(creation_date) BETWEEN "2025-06-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 30 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "press"
        AND DATE(creation_date) BETWEEN "2025-06-01" AND "2025-12-01"
    
UNION ALL

      SELECT domain_id, 0.97 AS percentage, 33 AS price, 1 AS renewed_count
      FROM radixbi-249015.radix_data.newreg
      WHERE mbg = 0
        AND LOWER(client_shortname) = "namecheap"
        AND tld = "host"
        AND DATE(creation_date) BETWEEN "2025-06-01" AND "2025-12-01"
    

      ;
      
      CREATE OR REPLACE TABLE npv_data.sensitivity_substitute AS
      SELECT
        domain_id,
        price,
        renewed_count,
        ROUND(EXP(SUM(LN(percentage))), 4) AS percentage -- Product of percentages
      FROM
        npv_data.sensitivity_substitute
      GROUP BY
        domain_id, price, renewed_count;
  

    

    -- Update the prediction table with new multiplying factor
    UPDATE
      npv_data.newreg_predictions_non_dp_20251229 a
    SET
      renew_prediction = ROUND(percentage * renew_prediction, 4)
    FROM
      npv_data.sensitivity_substitute d
    WHERE
      a.domain_id = d.domain_id
      AND a.revenue = d.price
      AND a.renewed_count = d.renewed_count
      AND a.renewed = 0
      AND DATE(creation_date) BETWEEN "2013-01-01"
      AND "2025-12-31";
  
```