---
title: 使用Git提交项目
date: 2017-10-18 09:10:23
tags: [GitHub, git]
categories: 经历记录
---

我在本地搭建了一个项目，想要提交到GitHub上，就在GitHub上建立了对应的Repository.

首先,打开命令行CD到本地项目下执行如下代码：	

```
git init
git add .
git commit -m "第一次提交"
```

至此执行一切正常；接下来我准备执行代码，提交到远程仓库：

```
git remote add origin git@github.com:yanzeyu9262/learningssm.git
git pull origin master
```

此时报错错误信息如下：

```
warning: no common commits
remote: Counting objects: 4, done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), done.
From github.com:yanzeyu9262/learningssm
 * branch            master     -> FETCH_HEAD
 * [new branch]      master     -> origin/master
fatal: refusing to merge unrelated histories
```

简单的阅读之后发现应该是存在冲突了，想起来我在远程添加了License和README文件。查阅了git相关命令执行如下代码：

```
git pull origin master --allow-unrelated-histories
```

执行更新成功，填写备注，接下来执行推送命令：

```
git push
```

终于上传项目成功。

ps：中间我还做了一次上传链接，执行命令如下：

```
git branch --set-upstream-to=origin/master master
```

