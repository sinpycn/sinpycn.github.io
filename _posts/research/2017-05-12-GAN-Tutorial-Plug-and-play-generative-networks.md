---
title: GAN介绍 - 即插即用生成网络
layout: post
mathjax: true
categories: [research, gan-tutorial]
---

[制作中]

在此辅导在NIPS被介绍不久前， 一个新的生成模型被发布了。 
这个模型， 即插即用生成网络 （Nguyen et al., 2016）, 非常引人注目的提高了ImageNet图像类的样本的多样性， 并且可以产品高分辨率的图像。

PPGN是新的并且还没有被理解。 
这个模型有点复杂， 并且多数推荐关于如何设计模型是基于经验观测， 而不是理论的理解。
此辅导将不会过多的讨论PPGN是如何工作的， 因为这可能会变得越来越明确在未来。

作为一个简洁的总结， PPGN是基本上一个近似 Langevin采样方法来产生图像 是哦那个马尔可夫链。
Langevin采样器的梯度被估计使用一个去噪autoencoder。
这个去噪的autoencoder被训练使用几个losses， 包含一个GAN loss。

图33展示了一些结果。 图34展示了，GAN loss对生成高质量的图片是很关键的。


![Figure 33](/images/201705/10/fig33.jpg)

![Figure 34](/images/201705/10/fig34.jpg)

