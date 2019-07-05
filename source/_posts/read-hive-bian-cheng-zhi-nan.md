---
title: 《hive编程指南》阅读
date: 2019-05-28 17:00:22
tags: [阅读, 心得]
categories: 阅读
---
1.对于管理表（内部表）来说，我们在hive中对表的操作，会影响到对应的数据文件；而对于外表，只会修改hive存储的元数据，不会影响文件系统中的文件。
2.alter table ... touch 钩子操作没看明白 待查
3.load data inpath '/path' overwrite into table name  会移动文件的位置，需要写权限
4.动态插入分区参数设置
'''
set hive.exec.dynamic.partition=true;
set hive.exec.dynamic.partition.mode=nonstrict;
set hive.exec.max.dynamic.partitions.pernode=1000;
'''