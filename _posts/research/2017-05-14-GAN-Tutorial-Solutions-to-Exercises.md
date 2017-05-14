---
title: GAN介绍 - 练习题答案
layout: post
mathjax: true
categories: [research, gan-tutorial]
---

[制作中]

## 8.1 最优的判别器策略

我们的目标是最小化

![Equation 23](/images/201705/10/eq23.jpg)

在函数空间， 直接指定$$D(x)$$。

我们开始通过假定$$p_{data}$$和$$p_{model}$$全局是非零。 如果我们不做此假设， 那么有些点将永远不会被访问到在训练过程中， 并且有不被定义的行为。

为了最小化关于D的J^{D}， 我们可以写下函数的导数，对应一个输入的D（x）， 并且将其设定为零：

![Figure 35](/images/201705/10/fig35.jpg)

图35： 一个展示关于判别器估计密度的比值。 在这个例子中， 为了简化起见， 我们假设z和x是一维的

通过解此方程， 我们得到

![Equation 24](/images/201705/10/eq24.jpg)

估计此比值是一个很重要的近似机制，使用GAN， 图35展示了此过程。

![Equation 25](/images/201705/10/eq25.jpg)


## 8.2 游戏的梯度下降

![Equation 26](/images/201705/10/eq23.jpg)

![Equation 27](/images/201705/10/eq27.jpg)

![Equation 29](/images/201705/10/eq29.jpg)

![Equation 30](/images/201705/10/eq30.jpg)


## 8.3 GAN框架中的最大似然

