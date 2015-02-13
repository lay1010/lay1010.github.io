---
layout: post
title: Mac上运行C++
category: 技术
tags: Mac
keywords: 
description: 
---

实验室里我申请的垃圾老爷机被师弟玩坏了，弄了一天，最后发现根本就是硬件有坏，想把它砸掉！太坑了。

clang是osx自带的c,c++,objective-c编译器；sublime就不多说了；本文的目的就是搭建一个轻量级的C++编辑-编译-调试-运行环境。


###方法一：
1. 打开sublime，`command`+`shift`+`P`
2. 输入install，选择`install package`，回车
3. 输入sublimeClang，回车下载
4. 编写一个简单的c++程序，保存为name.cpp
5. 在terminal中，`clang++ name.cpp -o name`
6. 双击name运行
7. 如果运行过程不需要输入数据，可以直接在sublime中`command`+`shift`+`B`运行


###方法二
1. AppStore中下载Xcode
2. 使用这个IDE



