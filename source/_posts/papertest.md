---
title: Java基础知识
date: 2017-11-15 14:50:37
tags: [Java, 常识]
categories: 知识积累
---

**前言**

工作有两年了，好多时候都显得不够专业，一些Java基础知识（或者说IT常识）都不能记得很清楚，为了让以后聊天时不尴尬，特此整理。

**基本概念**

· 操作系统中heap和stack的区别

栈（操作系统）：由操作系统自动分配释放。其操作方式类似于数据结构中的栈； 

堆（操作系统）： 一般由程序员分配释放，若程序员不释放，程序结束时可能由OS回收，分配方式倒是类似于链表。

[参考](http://blog.csdn.net/u014306011/article/details/51044091)

.事务的原则（ACID）

原子性（Atomicity）：事务是不可分割的，要么全执行要么全不执行

一致性（Consistency）：事务执行前后数据库的约束没有被破坏，业务逻辑也保持一致

隔离性（Isolation）：一个事务不应该影响其他的事务；

持久性（Durability）：事务提交后，会持久的保存到数据库，即使出现了事故

[参考](http://blog.csdn.net/shuaihj/article/details/14163713)

Cookie和Session的区别

Session是在服务端保存的一个数据结构，用来跟踪用户的状态，这个数据可以保存在集群、数据库、文件中；
Cookie是客户端保存用户信息的一种机制，用来记录用户的一些信息，也是实现Session的一种方式。

[参考](https://www.zhihu.com/question/19786827)

IO和NIO的区别

[参考](http://blog.csdn.net/evan_man/article/details/50910542)

远程通信的几种选择

[参考](http://blog.csdn.net/shan9liang/article/details/8995023)

