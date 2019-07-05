---
title: shell命令
date: 2019-06-20 17:23:11
tags: [shell, linux]
categories: shell
---
## 文件链接:ln命令
### 基本用法
```
ln from to 
```
这样会把from文件链接到to文件，from文件是原有的文件，to文件是新文件。添加链接之后会让文件的链接数+1，可以通过ls查看。

### tips
对于普通的链接来说，要保证是在同一个文件系统中，否则会报错。
不同文件系统的之间建立链接，可以添加“-s”参数，建立符号链接。
### 其他用法
```
ln files directory
```
把多个文件的链接放到到某个目录中。

## cut命令
```
cut -cchars file
cut -dchars -ffields file 
```
-c：可以指定多个范围
-d：指定分隔符
-f：指定取分割之后的第几个filed
## paste命令
```
paste files
paste -dchars files
paste -s 
```
-d：指定分隔符
-s：表示只从同一个文件中粘贴，如果只指定了一个文件，则将文件中所有的行合并到一行。
## sed命令（stream editor）
```
sed command file
```
