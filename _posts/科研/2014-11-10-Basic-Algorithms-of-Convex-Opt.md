---
layout: post
title: 凸优化的一些基础算法
category: 科研
tags: Optimization
keywords: 凸优化，基本算法
description: 
---

本文假设读者对凸优化有基本了解，主要归纳一些基础算法，以便查阅。

<a href="http://www.codecogs.com/eqnedit.php?latex=\min&space;f(x)&space;\triangleq&space;g(x)&plus;h(x)" target="_blank"><img src="http://latex.codecogs.com/gif.latex?\min&space;f(x)&space;\triangleq&space;g(x)&plus;h(x)" title="\min f(x) \triangleq g(x)+h(x)" /></a>

其中，f，g，h都是凸函数，g是光滑项，h是非光滑项。

###Gradient Descent
<a href="http://www.codecogs.com/eqnedit.php?latex=x^&plus;=x-\alpha\nabla&space;f(x)" target="_blank"><img src="http://latex.codecogs.com/gif.latex?x^&plus;=x-\alpha\nabla&space;f(x)" title="x^+=x-\alpha\nabla f(x)" /></a>
###Proximal Gradient
<a href="http://www.codecogs.com/eqnedit.php?latex=x^&plus;=prox_{\alpha&space;h}(x-\alpha&space;\nabla&space;g(x))=&space;\arg\min_u&space;h(u)&plus;\frac{1}{2\alpha}||u-x&plus;\alpha&space;\nabla&space;g(x)||" target="_blank"><img src="http://latex.codecogs.com/gif.latex?x^&plus;=prox_{\alpha&space;h}(x-\alpha&space;\nabla&space;g(x))=&space;\arg\min_u&space;h(u)&plus;\frac{1}{2\alpha}||u-x&plus;\alpha&space;\nabla&space;g(x)||" title="x^+=prox_{\alpha h}(x-\alpha \nabla g(x))= \arg\min_u h(u)+\frac{1}{2\alpha}||u-x+\alpha \nabla g(x)||" /></a>
###Conjugate Gradient

###Newton

###Quasi Newton