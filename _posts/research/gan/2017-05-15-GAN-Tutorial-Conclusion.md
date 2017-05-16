---
title: GAN介绍 - 总结，鸣谢
layout: post
mathjax: true
categories: [research, gan-tutorial]
---

# 总结

GAN是使用有监督学习来优化一个难以控制的损失函数的生成式模型， 很像玻尔兹曼机(Boltzmann machine)使用马尔可夫链(Markov chain)来优化他们的损失函数， 
以及VAE使用变分低边界(variational lower bound)来优化他们的损失函数。
GAN可以使用此有监督的比值估计技术，来近似很多的损失函数， 包括最大似然估计使用的KL散度。

GAN是相对很新的技术，并且仍然需要很多的研究来挖掘它的潜力。
特别的，训练GAN需要在高维，连续，非凸的游戏中找到纳什均衡。
研究者可以尝试开发更好的理论来理解GAN，以及为GAN场景开发更好的训练算法。
这方面的成功会不仅对GAN，对解决很多的其他应用都会有帮助。

GAN是很关键的对很多先进的图像生成，以及处理系统， 并且未来还有很多的潜力在很多其他应用上。

# 鸣谢
作者感谢NIPS组织者的对此次辅导的邀请。 并且特别感谢在Twitter和Facebook上针对辅导内容给出留言和建议的网友们。
另外感谢D. Kingma关于VAE描述的宝贵的讨论。并且感谢Zhu Xiaohu, Alex Kurakin和Ilya Edrenkin指出本资料中的拼写错误。

# 参考文献
（请参考原英文文章）
