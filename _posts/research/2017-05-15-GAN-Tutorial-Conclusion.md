---
title: GAN介绍 - 总结，鸣谢
layout: post
mathjax: true
categories: [research, gan-tutorial]
---

[制作中]

# 总结

GAN是生成式模型，使用监督学习来优化一个难以控制的损失函数， 很像Boltzmann machine使用Markov chain来优化他们的损失函数， 
以及VAE使用变分低边界来优化他们的损失函数。
GAN可以使用有监督的比值估计技术，来近似很多的损失函数， 包括使用KL divergence的最大似然估计。

GAN还很新，并且仍然需要很多的研究来挖掘它的潜力。
特别的，训练GAN需要找到纳什均衡，在高维，连续，非凸的游戏中。
研究者应该试着开发更好的理论理解以及更好的训练算法为GAN。
这种成功会对很多应用有提升，除了GAN。

GAN是很关键的对很多先进的图像生成，以及处理系统， 并且未来还有很多的潜力在很多其他应用上。

# 鸣谢
作者感谢NIPS组织者的邀请，
The author would like to thank the NIPS organizers for inviting him to present
this tutorial. Many thanks also to those who commented on his Twitter and
Facebook posts asking which topics would be of interest to the tutorial audience.
Thanks also to D. Kingma for helpful discussions regarding the description of
VAEs. Thanks to Zhu Xiaohu, Alex Kurakin and Ilya Edrenkin for spotting
typographical errors in the manuscript.
