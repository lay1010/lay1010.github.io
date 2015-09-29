---
layout: post
title: 从二次型最优化问题中理解矩阵特征值的意义
category: 科研
tags: Math Optimization 
keywords: 特征值
description: 
---

###惯例开场故事
在某次从实验室去往食堂的路上，曾发生这样一段对话：

『大师兄，为什么你对算法的理解总是那么透彻呢？为什么我很难看出它背后的思想？』

『因为你去理解一个算法的时候，不能只是看懂它的形，还要去思考它的神啊~』

这就是我天分不够当不了科学家的佐证吧T。T

###例子1：二次型最优化
最小化二次型目标函数<a href="http://www.codecogs.com/eqnedit.php?latex=f(x)=x^TAx" target="_blank"><img src="http://latex.codecogs.com/gif.latex?f(x)=x^TAx" title="f(x)=x^TAx" /></a>，其中，<a href="http://www.codecogs.com/eqnedit.php?latex=A=[1,0.5;0.5,1]" target="_blank"><img src="http://latex.codecogs.com/gif.latex?A=[1,0.5;0.5,1]" title="A=[1,0.5;0.5,1]" /></a>，<a href="http://www.codecogs.com/eqnedit.php?latex=x=[x_1,x_2]^{\textrm{T}}&space;\in&space;\textcal{R}^2" target="_blank"><img src="http://latex.codecogs.com/gif.latex?x=[x_1,x_2]^{\textrm{T}}&space;\in&space;\textcal{R}^2" title="x=[x_1,x_2]^{\textrm{T}} \in \textcal{R}^2" /></a>.这个问题的求解很简单，这里以此为例来说明该问题与矩阵特征值的关系。

首先，可以得到目标函数的网格图与等高线图如下。

![1](/public/img/posts/mesh_of_f.png)
![2](/public/img/posts/contour_of_f.png)

对矩阵A进行特征分解可以得到其特征向量为[-0.7071, 0.7071], [0.7071, 0.7071]，对应的特征值分别是0.5, 1.5.

观察函数的等高线图可以知道，等高线最密集的地方，函数值变化最快，而这个函数值变化最快的方向归一化后就是[0.7071, 0.7071]，这恰好是矩阵的一个特征向量。同样地，可以观察，等高线最稀疏的地方，函数值变化最慢，变化方向则是矩阵的另一个特征向量。

进一步，我们总是可以对A进行相似变化得到一个以A的特征值为对角线元素的对角阵B。把目标函数改写为<a href="http://www.codecogs.com/eqnedit.php?latex=f(x)=x^{\textrm{T}}P^{-1}BPx" target="_blank"><img src="http://latex.codecogs.com/gif.latex?f(x)=x^{\textrm{T}}P^{-1}BPx" title="f(x)=x^{\textrm{T}}P^{-1}BPx" /></a>，其中<a href="http://www.codecogs.com/eqnedit.php?latex=B=[0.5,&space;0;&space;0,&space;1.5]" target="_blank"><img src="http://latex.codecogs.com/gif.latex?B=[0.5,&space;0;&space;0,&space;1.5]" title="B=[0.5, 0; 0, 1.5]" /></a>. 相似变换的作用可以理解为将等高线图进行旋转，于是得到下面经过旋转后的等高线图。

![3](/public/img/posts/contour_of_f_B.png)

在这张图上说明矩阵特征值的意义。（未完待续）




###资料

【1】[如何理解矩阵特征值](http://www.zhihu.com/question/21874816/answer/19592526)



