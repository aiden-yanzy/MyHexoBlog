---
title: 使用mame模拟器
date: 2018-10-19 14:08:38
tags: [mame, game]
categories: 经历记录
---
    	
# 前言
有一天中午和同事一起吃完饭之后聊起了儿时玩过的游戏，想到了拳皇、街霸、双截龙、热血系列等等，种种回忆历历在目，所以有了重温哪些游戏的想法。上网搜索之后选择了mame，mame是一个功能强大的模拟器，当然真正用起来的时候还是遇到了一些问题，主要是bios缺失。
最近换了manjaro系统，我的安装都是基于此系统的。

## 安装mame   	    
+ Manjaro安装mame，直接用pacman命令安装最新的软件，我安装的版本是0.202.
    
		sudo pacman -Sy mame

>其实这不是太好的方式，会导致bois的缺失。也就是我之后遇到的问题。比较好的方式在一个英文网站有介绍，网站链接：[https://journalxtra.com/mame/download-complete-sets-of-mess-and-mame-roms/](https://journalxtra.com/mame/download-complete-sets-of-mess-and-mame-roms/)。

## 安装rom
   
+ 下载 rom网站还是挺好找的，但是合集好少。推荐一个网址：[街机中国 http://www.mamecn.com/](http://www.mamecn.com/)。

+ 移动下载好的文件一般是\*\.zip，到mame的roms目录。我的目录是：~/.mame/roms

		sudo cp ~/Download/kof98.zip ~/.mame/roms

+ 运行mame选择相应游戏就可以玩耍了。或者命令行执行
	
		mame kof98

>不幸的是在运行kof98的时候报错了，当时没有截图就不放了，但是大意就是缺少\[neogeo\]。google了好久最后还是在街机中国找到了我需要的包。论坛地址：[0.202 Bios](http://bbs.mamecn.com/viewthread.php?tid=17786)。
另外附上我下载的包[mame_202_bios.7z](mame_202_bios.7z)。

+ 将上边下载的bios包也解压到~/.mame/roms,就可以正常游戏了。

# 写在最后
配置手柄的时候可以在进入到游戏时按tab呼出配置菜单，可以设置通用配置也可以对每个游戏单独设置，重置配置的话直接删除"/.mame/cfg/"目录下的对应配置就ok了（default配置是全局配置）。
