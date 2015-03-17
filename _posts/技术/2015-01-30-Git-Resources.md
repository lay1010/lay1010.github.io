---
layout: post
title: Git常用资源
category: 技术
tags: Git
keywords: 
description: 
---

###1.1 在工作目录中创建新仓库
进入新建的目录GitTest

```
$ git init
```

###1.2 检查状态

```
$ git status
```

###1.3 添加与提交
在当前工作目录中创建文件，这里我新建了`ReadMe.md`

###1.4 添加变化

```
$ git add ReadMe.md
```

###1.5 检查变化

```
$ git status
```

###1.6 提交

```
$ git commit -m "Add ReadMe"
```

###1.7 添加所有变化
比如添加所有的`.md`文件

```
$ git add '*.md'
```
###1.8 提交所有变化

```
$ git commit -m 'Add all md files'
```

###1.9 历史
```
$ git log
```

###1.10 远程仓库
```
$ git remote add TestGit https://github.com/lay1010/TestGit.git
```
注意：按照官方教程，命令是`add origin`，而我之前已经误用过`origin`这个名字了，如果仍然git remote add origin，会出现fatal：remote origin already exists.

解决办法：将origin更换为其他名字，比如我现在更换为TestGit，后面的命令也相应地把origin替换为TestGit。感谢一楼评论`小明 曹`童鞋。

###1.11 远程推送
```
$ git push -u TestGit master
```

###1.12 远程拉入
```
$ git pull TestGit master
```

###1.13 区别
```
$ git diff HEAD
```

###1.14 阶段区别
```
$ git add testfamily/3.md
$ git diff --staged
```
`3.md`是刚刚添加的文件。


###1.15 重置阶段
```
$ git reset testfamily/3.md
```
移除3.md，注意这里只是将3.md从staged状态移除。

###1.16 撤销
```
$ git checkout -- 2.md
```
注意：checkout的用法不是很懂，这儿得问问。

###1.17 分支出去
```
$ git branch clean_up
```
创建一个名叫`clean_up`的分支。

###1.18 切换分支
```
$ git checkout clean_up
```
从master切换到了clean_up

###1.19 移除所有东西
```
$ git rm '*.md'
```

###1.20 提交分支变化
```
$ git commit -m "remove all things"
```

###1.21 切换回master分支
```
$ git checkout master
```
###1.22 准备合并分支
```
$ git merge clean_up
```
###1.23 保持简洁（删除分支）
```
$ git branch -d clean_up
```
###1.24 最终推送
```
$ git push
```
推送所有东西。

注意：完成所有步骤后发现blog里面所有的文件都消失了。原因我也不知道，看来看是得系统看书去。

###1.25 退回到之前1天的版本
```
$ git log --before="1 days"
```


###资料链接
1. [Try Git](https://try.github.io/levels/1/challenges/1)



