---
title: "An Empirical Evaluation of Thompson Sampling"
layout: page
date: 2019-07-31
---

汤普森采样启发式、易实现、理应作为基线

### 1、什么是TS

- **什么是EE**——利用历史数据获取收益的同时，对未知数据进行探索（带来累计遗憾），逼近全局最优
- **为什么Beta分布**——二项式分布的共轭先验

![屏幕快照 2019-07-30 下午8.02.57](/Users/yunxiaofeng/github/wiki/themes/simple2/static/image/屏幕快照 2019-07-30 下午8.02.57.png)



举例

![屏幕快照 2019-07-30 下午7.22.08](/Users/yunxiaofeng/github/wiki/themes/simple2/static/image/屏幕快照 2019-07-30 下午7.22.08.png)



### 2、文章重点

对与先验满足高斯分布，而后验不满足的情况，做拉普拉斯近似，如下

![屏幕快照 2019-07-31 上午11.48.29](/Users/yunxiaofeng/github/wiki/themes/simple2/static/image/屏幕快照 2019-07-31 上午11.48.29.png)

上式子用来近似原分布**（参数的后验分布）**



![屏幕快照 2019-07-30 下午8.59.30](/Users/yunxiaofeng/github/wiki/themes/simple2/static/image/屏幕快照 2019-07-30 下午8.59.30.png)

- **更新分布参数前，w如何取最小值**——minimize指做完gradient descent之后
- **为什么对上式直接取二阶导**——表达式对应参数（w）后验分布取log，满足拉普拉斯近似中海森矩阵在单变量下的表达式

- **W为什么服从高斯分布**
