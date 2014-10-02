---
layout: post
title: 阿里巴巴大数据竞赛回顾与总结
category: 科研
tags: 大数据 机器学习
keywords: 大数据，机器学习，推荐系统
description: 
---

今年2月的某天，苏宇师兄问我对[阿里巴巴大数据竞赛](http://102.alibaba.com/competition/addDiscovery/index.htm)感兴趣吗，那时我学完[陈恩红](http://staff.ustc.edu.cn/~cheneh/)老师的《机器学习与数据挖掘》课程没多久，很好奇课程内容在实际中的应用。身为淘宝用户，也好奇我是如何被推荐的，学以致用嘛，于是就答应了和师兄一起参加比赛。正好那会儿认识了计算机学院的[刘惠民](http://painterliu.com)同学（FYI：他的个人博客风格设计是抄袭我的-。-），很快我们就组成了三人行团队，为团队起名`Rosemary`。

###赛题介绍
本赛题适用于season1 和season 2的比赛，season 3 为线上赛（season 2 赛后公布题目）。 
在天猫，每天都会有数千万的用户通过品牌发现自己喜欢的商品，品牌是联接消费者与商品最重要的纽带。本届赛题的任务就是根据用户4个月在天猫的行为日志，建立用户的品牌偏好，并预测他们在将来一个月内对品牌下商品的购买行为。

开放数据如下：

<table  class="table table-bordered table-striped table-condensed">
   <tr>
     <th>字段</th>
      <th>字段说明</th>
      <th>提取说明</th>
   </tr>
   <tr>
      <td>user_id</td>
      <td>用户标记</td>
      <td>抽样、字段加密</td>
   </tr>
   <tr>
      <td>Time</td>
      <td>行为时间</td>
      <td>精度到天级别、隐藏年份</td>
   </tr>
   <tr>
      <td>action_type</td>
      <td>用户对品牌的行为类型</td>
      <td>包括点击（0）、购买（1）、加入购物车（2）、收藏（3）四种行为 </td>
  </tr>
   <tr>
      <td>brand_id</td>
      <td>品牌数字ID</td>
      <td>抽样、字段加密</td>
   </tr>
</table>
用户对任意商品的行为都会映射为一行数据。其中所有商品ID都已汇总为商品对应的品牌ID。用户和品牌都分别做了一定程度的数据抽样，且数字ID都做了加密。所有行为的时间都精确到天级别(隐藏年份)。

###评估指标
希望参赛队的预测, 预测的品牌准确率越高越好，也希望覆盖的用户和品牌越多越好，所以用最常用的准确率与召回率作为排行榜的指标。

准确率：<img src="http://chart.googleapis.com/chart?cht=tx&chl=Precision%3D%5Cfrac%7B%5Csum_i%5EN%20hitBrands_i%7D%7B%5Csum_i%5EN%20pBrands_i%7D" style="border:none;" />

注： 

- N 为参赛队预测的用户数 
- pBrandsi为对用户i 预测他(她)会购买的品牌列表个数 
- hitBrandsi对用户i预测的品牌列表与用户i真实购买的品牌交集的个数

召回率：<img src="http://chart.googleapis.com/chart?cht=tx&chl=Recall%3D%5Cfrac%7B%5Csum_i%5EM%20hitBrands_i%7D%7B%5Csum_i%5EM%20bBrands_i%7D" style="border:none;" />

注：

- M 为实际产生成交的用户数量 
- bBrandsi为用户i 真实购买的品牌个数 
- hitBrandsi预测的品牌列表与用户i真实购买的品牌交集的个数

最后用F1-Score 来拟合准确率与召回率，并且大赛最终的比赛成绩排名以F1得分为准。

F1-Score：<img src="http://chart.googleapis.com/chart?cht=tx&chl=F_1%3D%5Cfrac%7B2PR%7D%7BP%2BR%7D" style="border:none;" />

好了，比赛信息大致如上。简单说就是天猫给我们数据，我们需要在有限的数据中学习出所需要的东西，这里就是根据天猫用户在过去4个月的行为记录去预测下1个月他们的购买行为与购买品牌。

###拿到题目后的分析

（好困，需要去睡觉Zzz···）未完待续

###第一赛季

###第二赛季

###成绩排名

第一赛季排名：56/all7276;（没有截图）

第二赛季排名：68/top500.（截图纪念）

![1](/public/img/score0.png)


###总结


