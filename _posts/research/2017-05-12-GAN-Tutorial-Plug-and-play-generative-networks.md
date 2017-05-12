---
title: GAN介绍 - 即插即用生成网络
layout: post
mathjax: true
categories: [research, gan-tutorial]
---

[制作中]

在此辅导在NIPS被介绍的不久前， 一个新的生成模型被发布了。 
这个网络， 即插即用生成网络 （Nguyen et al., 2016）, 非常引人注目的提高了ImageNet图像类的样本的多样性， 并且可以产生高分辨率的图像。

PPGN是一个新的工作，并且还没有被很好理解的。 
这个模型有点复杂， 并且多数建议关于如何设计模型是基于经验观察而不是理论的理解。
此辅导将不会过多的讨论PPGN是如何工作的， 因为在不久的将来这会变得越来越清晰。

作为一个简洁的总结， PPGN是基本上一个近似Langevin采样方法使用马尔可夫链来产生图像。
Langevin采样器的梯度被估计使用一个降噪的（denoising） autoencoder。
这个降噪autoencoder被通过几个损失函数来进行训练， 其中包含一个GAN损失函数。

图33展示了一些结果。 图34展示了，GAN loss对生成高质量的图片是很关键的。

![Figure 33](/images/201705/10/fig33.jpg)

图33： PPGN可以产生反转的， 高分辨率的ImageNet图像。 图片来自Nguyen et al. (2016).

![Figure 34](/images/201705/10/fig34.jpg)

图34： GAN的损失函数PPGN显著的组成部分。 没有它， PPNG使用的降噪autoencoder将不能产生高质量的图像。

