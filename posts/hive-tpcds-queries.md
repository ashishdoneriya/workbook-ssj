---
title : "Hive tpcds query"
created : "2019-09-04T03:17:00+05:30"
updated : "2019-09-04T03:17:00+05:30"
categories : ["software-engineering"]
tags : ["hive"]
summary : "Hive tpcds query"
---

Database :  
tpcds_bin_partitioned_orc_60


```sql
select  dt.d_year, item.i_brand_id brand_id, item.i_brand brand, sum(ss_ext_sales_price) sum_agg from  date_dim dt, store_sales, item where dt.d_date_sk = store_sales.ss_sold_date_sk and store_sales.ss_item_sk = item.i_item_sk and item.i_manufact_id = 436 and dt.d_moy=12 group by dt.d_year, item.i_brand, item.i_brand_id order by dt.d_year, sum_agg desc, brand_id limit 100;
```
