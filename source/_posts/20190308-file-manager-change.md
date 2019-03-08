---
title: 安装vscode之后manjaro默认的资源管理器被替换
date: 2019-03-08 15:17:46
tags: [manjaro, vscode, 文件系统， linux]
categories: 问题解决
---
最近vscode这个编辑器很火，所以在自己的manjaro系统安装了一个，但是安装之后发现在chrome中下载了文件，选择在文件夹打开之后会进入到vscode中，删除vscode之后恢复正常。
网上搜索了一下终于找到了解决方案，亲测有效，现在记录一下。
首先是查看现在的资源管理器，在terminal中输入如下命令。
```
xdg-mime query default inode/directory
```
显示结果如下，果然是变成了vscode。
```
visual-studio-code.desktop
```
还原为manjaro的指令如下。
```
xdg-mime default org.gnome.Nautilus.desktop inode/directory
```

参照的文章地址为：
[https://blog.csdn.net/qq_32337527/article/details/81778732](https://blog.csdn.net/qq_32337527/article/details/81778732)