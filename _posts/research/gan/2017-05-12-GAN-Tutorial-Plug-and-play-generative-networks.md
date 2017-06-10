---
title: GAN介绍 - 即插即用生成网络(PPGN)
layout: post
mathjax: true
categories: [research, gan-tutorial]
---

此辅导在NIPS被介绍的不久前， 一个新的生成模型，即插即用生成网络(PPGN: Plug and Play Generative Networks) （Nguyen et al., 2016）,被发布了。 此网络非常引人注目的提高了ImageNet上图像类的样本多样性， 并且可以产生高分辨率的图像。

PPGN是一个新的工作，并且还没有被很好的理解。 
这个模型有点复杂， 并且多数的关于如何设计模型的建议是基于经验性的观察而不是理论的理解。
此辅导将不会过多的讨论PPGN是如何工作的， 因为在不久的将来这会变得越来越清晰。

作为一个简洁的总结， PPGN总的来说是通过近似Langevin采样方法，使用马尔可夫链来产生图像。
Langevin采样器的梯度通过使用一个降噪的（denoising） 自动编码器来估计。
这个降噪自动编码器使用几个损失函数来进行训练， 其中包含一个GAN的损失。

图33展示了一些结果。 图34展示了GAN loss对生成高质量的图片是很关键的。

![Figure 33](/images/201705/10/fig33.jpg)

图33： PPGN可以产生反转的， 高分辨率的ImageNet图像。 图片来自Nguyen et al. (2016).

![Figure 34](/images/201705/10/fig34.jpg)

图34： GAN的损失是PPGN显著的组成部分。 没有它， PPNG使用的降噪自动编码器将不能产生高质量的图像。


[最终修改于： 2017年6月10日]
