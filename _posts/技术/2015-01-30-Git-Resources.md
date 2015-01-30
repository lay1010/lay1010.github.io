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
$ git remote add origin https://github.com/try-git/try_git.git
```
注意：这里出现fatal：remote origin already exists.我暂时没能解决。

###1.11 远程推送
```
$ git push -u origin master
```
出现fatal：Repository not found.

###1.12 远程拉入
```
$ git pull origin master
```

错误一直没能解决，先去看看progit再来更新。

###资料链接
1. [Try Git](https://try.github.io/levels/1/challenges/1)








