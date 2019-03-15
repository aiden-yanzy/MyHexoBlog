---
title: hive工作拾遗20190314
date: 2019-03-14 15:21:17
tags: [hive, 工作记录， 知识累积]
categories: 工作记录
---
昨天写sql是用用到了“sum(b.user_gmv) OVER (ORDER BY b.user_gmv DESC ROWS BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW)”语法，在最开始是的时候，因为看到网上有博客写如果计算的是从第一行到当前行时加不加窗口的结果是一样的，所以我没有添加窗口“BETWEEN UNBOUNDED PRECEDING AND CURRENT ROW”。然而我每次执行语句的时候，总是卡在reduce执行到78%的时候。后来添加了窗口，很快就跑过去了，看来是否添加窗口得出的结果虽然一致，但是过程不太一样呢。
具体的原因之后，在仔细研究一下吧。