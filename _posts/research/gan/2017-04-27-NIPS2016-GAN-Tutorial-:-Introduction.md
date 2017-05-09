---
title: GAN介绍 - 介绍
layout: post
mathjax: true
categories: [research, gan-tutorial]
---

### 前言

首先特别感谢Ian Goodfellow先生对此翻译工作的许可与支持。 
此翻译工作是我本人为了更好的学习GAN的相关技术而制作的。
通过学习此资料， 可以帮助我们更全面的了解GAN相关的基础知识。 
对于要学习GAN，以及打算使用GAN做进一步工作的同学，此资料是不可或缺的。

此材料是根据Goodfellow先生二个小时演讲的内容而整理制作的，所以对有些内容的描述不够全面。
关于一些被省略的相关内容， 后续，我会有选择的进行补充介绍。 
另外此翻译版本也对原文中的部分章节进行了删减。

此材料主要包含有以下几个方面的内容：

1. 为什么需要学习生成式建模？
2. 生成式模型是如何工作的？ GAN与其他生成式模型有什么区别？
3. GAN是如何工作的？
4. 提示与技巧
5. GAN的相关研究课题
6. 即插即用生成模型
7. 练习
8. 练习解答
9. 结论

### 介绍 
从分类上来说，GAN属于生成式模型。 生成式模型有很多的不同的应用方式， 此处的生成式模型指的是用某种方式去学习并表达针对一个训练数据集分布的估计，也就是 $$p_{model}$$， 因为对于一个训练数据集来说，它所包含的样本会满足一定的分布 $$p_{data}$$。

有的情况下， 模型的目的是去显式的估计$$p_{model}$$，比如图1。 
还有的情况下， 模型只能通过 $$p_{model}$$ 来产生样本，如图2。 
还有模型可以兼而有之。 GAN主要针对样本生成，尽管也可以设计GAN去做此两者。

![Figure 1](/images/201704/28/fig01.png)

图1： 有些生成式模型通过密度估计。 这类模型通过从未知的数据分布 $$p_{data}$$ 生成数据来获取更多的训练数据样本, 并且得到对此未知分布的估计。 通常情况下， 我们不可能知道真实的数据分布 $$p_{data}(x)$$， 只能通过一些特殊的样本 $$x$$ 来对训练模型 $$p_{model}$$ 来实现对真实数据密度的一个估计。 
此图展示了一个一维的数据和一个针对此数据分布的高斯模型。

![Figure 2](/images/201704/28/fig02.png)

图2： 一些生成式模型可以通过模型的分布来产生样本。 此图展示了ImageNet的样本。 理想的情况下，生成式模型可以使用左边的样本进行训练， 然后产生更多的相同分布的样本 （见右边）。 （由于当前的生成式模型还不能很好的完成对ImageNet样本的生成，此图中右边的样本使用了真实的ImageNet样本来说明此方法。）