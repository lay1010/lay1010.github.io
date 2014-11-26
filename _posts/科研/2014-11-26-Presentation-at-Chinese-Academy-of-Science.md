---
layout: post
title: 我在中科院数学与系统科学研究院的报告总结
category: 科研
tags: Math Optimization
keywords: 报告总结
description: 
---

###
这学期我在中科院数学与系统科学研究院访问。第一次参与这边的讨论班，我就被震惊了：纳尼学生做报告也全英文啊？事后想想还是正常，毕竟都是我的新晋男神[袁亚湘](http://lsec.cc.ac.cn/~yyx/chinese/indexc.htm)老师的学生。因此，11月25日，我也在这儿完成了自己这辈子第一次的英文“学术”报告。

我想说两件事儿：

1. 报告前3天，我问盛镇醴师兄：“你们做报告之前会排练吗？”，因为当时我在犹豫要不要自己对着镜子练几遍。师兄说：“肯定啊！我们上次去葡萄牙开会，要做报告，我因为之前讲过报告就不想再练习了，但[马士谦](http://www.se.cuhk.edu.hk/people/sqma.html)师兄，他已经讲得那么好了，都还又自己练习了5、6遍。师兄真的可以做到每句话精确到几秒钟！”那一刻，我又一次深深体会到，这个世界上那么多“比你聪明的人，还比你踏实，比你努力”。像自己这种又笨又懒的人还活得下去？
2. 于是我也私下练习了两次。果然还是努力了内心就会踏实，在当天的报告中，我不仅丝毫不紧张，反而在某个间隙一瞅台下一堆人正深情专注地看着我和我的幻灯片时，心里突然弹幕全开“哇，原来让一堆人听我说话是这感觉，哇，这感觉好爽啊~~~，哇，袁老师也在看，嗯，自己英文还挺流利的...”而我清楚地知道，这一切positive的心情，都是因为私下的努力。

我想记录一下那一天的报告。顺便插播一段回忆：
大三暑假，我参加[中国大学生物联网创新创业大赛](http://china.ican-contest.org/index.html)，正式比赛前一天系里组织答辩练习，我们组讲得一塌糊涂。那一晚，我和向国菲师兄在实验室通宵改PPT，准备发言稿，然后一句一句地练习。中途师兄压力太大又累得不行溜出去躲着抽了根烟，回来被我发现了教育了一顿，嗅觉就是这么灵敏哈哈。直到凌晨4点，终于觉得还算满意了，两人躺椅子上睡了会儿，当然我被蚊子咬安逸了。早晨7点，寝室开门，两人各自回去洗澡调整状态，9点，开始比赛。不知道为什么突然浮出这个片段，太，美好了。尽管当时觉得真苦逼。

![1](/public/img/posts/s1.png)




###Page 1
- Good afternoon everyone! My name is Anya Lin. I'm a second-year master candidate from University of Science and Technology of China. It's my great pleasure to introduce to you the Decentralized Privacy-Preserving Low-Rank Matrix Completion. It's a joint work with my supervisor, Prof. Ling from USTC.
- Before I start, I want to express my thanks to Prof. Ling for his patient instructions and help over the last a few months.

###Page 2
- Here's the outline of my presentation.
- First is the introduction.
- And then the centralized matrix completion problem.
- We develop a decentralized algorithm in section 3, and our algorithm is derived from a centralized algorithm as I will talk about in section 2.
- Next, I will introduce the main result of the topology-dependent privacy preservation.
- At last, it's the conclusion.

###Page 3
- OK， let's go into the introduction.

###Page 4
- I'd like to begin with the concept of matrix completion. So what is matrix completion? As we can see in this picture, we have an incomplete matrix, whose entries are known only for a subset of the whole matrix. And the rank of the matrix is very small compared with the size of the matrix.
- The goal of the matrix completion is to recover all these unknown entries of of the matrix, as the right-side picture shows. Here, Z is the recovery of W.

###Page 5
- There's many applications of such a problem. Like image processing, recommendation system and so on. Here are 2 examples. The first one is a problem of image processing. The left picture has a lot of noises, or say, only a part of the original picture is known. By using the fact that the original picture is usually low-rank, we can matrix completion to denoise the picture and get a clear version of high quality as the right picture shows.
- The second example is more close to our lives. It's related to a recommendation system. As you can see, it's a webpage of Douban Movie. A user sees a movie, such as Interstella, and then scores it on the website. Here we can imagine a huge matrix with rows representing users and columns the movies. This matrix is incomplete and it's low-rank. Once this matrix is completed, the website can recommend new movies to users.

###Page 6
- Now, here comes a privacy concern. First what is privacy? Privacy is the values one considers private. In the example we mentioned just now, the users' scores of the movies are privacy, because one may not want others to know what movies he has seen or likes. Also, the entries of the matrix could be medical records of patients, or selling data of merchants. These data are considered as privacy.
- Obviously, no one wants the leakage of his privacy.
- However, in reality there may exist a malicious agent, a bad guy. For some reasons you have to give your private data to it, but you don't know wether you can trust it or not.
- In this situation, we need privacy-preservation. Privacy-preservation is the ability to prevent a malicious agent from obtaining or reconstructing the private data.

###Page 7
- Now let's go into the centralized matrix completion problem.

###Page 8
- When we are faced with a low-rank matrix completion problem, the intuitive thought would be to minimize the rank of the matrix, but this is a nonconvex problem. 
- Therefore, we insteadly minimize the nuclear-norm the the matrix, since nuclear-norm is the approximation of the rank and it's convex.
- Another approach is if the rank of matrix is known to be r as a prior theoreticallyor empirically, we can get the matrix factorization formulation. This approach is advantageous over the nuclear-norm approach since the latter one needs sigular value decomposition, which is computationally expensiven and even intractable in decentralized computing.
- A centralized algorithm call LMaFit to solve this is as the following steps shows.
- We have to keep in mind that our algorithm is derived from LMaFit.

###Page 9
- After the centralized problem, let's go into the decentralized one.

###Page 10
- In decentralized computing, we have a network composed of L agents.
- There is an undirected edge between two agents if they can communicate with each other through one hop.
- The goal of all the agents in such a network is to collaboratively complete a low-rank matrix in a decentralized fashion.

###Page 11
- To be specific, we segment the whole data matrix W into groups of columns. And do the same to Y and Z. Each agent i in the network holds the corresponding Zi, Yi and entries of Wi. 
- However, X cannot be segmented and distributed to agents because the update of X contains the summation of ZiYi' over all agents. So we let each agent i holds a local copy X(i) of X.
- After doing this, we get a naive decentralized implementation of LMaFit. At iteration k, each agent i does the following steps respectively.
- Notice that the update of X requires information aggregation of all agents. So here is the challenge: informationaggregationofallagentsisimpossible in real decentralized network unless every agent is connected to all the other agents. 
- How to deal with this challenge?

###Page 12
- The answer is dynamic average consensus. Recall that each agent i holds a local copy X(i) of X. If we can make sure that X(i) equals to X for all i, the challenge is solved. 
- To do this, we choose c to be 1/L and the update of X becomes the average consensus problem, as we can see in equation (8), X(i) is the average of all the ZiYi'.
- At iteration k,we formulate the average consensus problem as equation (9). The constraint means that instead of letting all the X(i) to be identical we choose to let each X(i) equals to it neighboring X(j).
- A key observation is that exact average consensus at every iteration is not necessary. We use EXTRA2 to do inexact dynamic average consensus, which saves the computational cost.

###Page 13

(to be continued)


啊，怎么写了这么久都还写不完啊。。。。。。。我要休息了。。。。。下回来补充完整。




###对我有帮助的资料
【1】[有哪些高级的英语表达技巧，让人一听就很地道？](http://www.zhihu.com/question/24544386/answer/30237316)



