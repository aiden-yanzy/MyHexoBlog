---
title: hive工作拾遗20190313
date: 2019-03-13 11:25:16
tags: [hive, 工作记录， 知识累积]
categories: 工作记录
---
今天开始工作重心切换到了数据统计方面，需要写hql生成统计表。由于hive执行的速度比较慢，加上想要记录工作收获，所以边工作边记录一下。
 
 使用到的命令等
 1. 建立临时表,与sql类似
    ```
    create table_name as select col_a, col_b from origin_table where condition=true;
    ```

 2. 使用hive分析函数，sum() over(),没想到是从一个日文网站找到了例子。[https://qiita.com/tlokweng/items/fc13dc30cc1aa28231c5](https://qiita.com/tlokweng/items/fc13dc30cc1aa28231c5)
    ```
      SELECT order_id, item, COUNT(*) OVER (PARTITION BY item) FROM test_orders ORDER BY order_id;
      select order_id, item, count(*) over (order by order_id) from test_orders;
      SELECT order_id, item, qty, SUM(qty) over (PARTITION BY item ORDER BY order_id) FROM test_orders;
      SELECT order_id, item, qty, SUM(qty) OVER (ORDER BY order_id ROWS BETWEEN 1 PRECEDING AND 1 FOLLOWING) result FROM test_orders;
    ```

3. 根据查询结果插入表
   ```
      INSERT OVERWRITE TABLE schema_name.table_name 
      SELECT column_names FROM source_schema_name.source_table_name;
   ```
今天跑的数，总是reduce到78%就进行不下去了，看来需要进行优化。
