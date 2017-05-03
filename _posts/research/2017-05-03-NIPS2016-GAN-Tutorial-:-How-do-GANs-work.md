---
title: GAN Tutorial - How do GANs work?
layout: post
mathjax: true
---

[制作中]
我们已经了解了GAN与其他生成模型的区别，下面我们将学习GAN是如何工作的。

## 3.1 GAN framework

GAN的基本思想是两个玩家共同玩一个游戏。 其中一个叫生成器。 生成器根据训练数据的分布来生成样本。 另一个玩家是判别器。 判别器用来判别样本的真伪。
判别器使用传统的监督学习的方法，将输入分类为真和假两个类。 生成器被优化来试图欺骗判别器。
举个例子来说， 生成器类似于假币制造者，他试图制作假币， 判别器类似于警察， 他试图判别真币和假币。 
为了在游戏中取得成功， 造假者必须

![Figure 12](/images/201705/03/fig12.jpg)

![Figure 13](/images/201705/03/fig13.jpg)

## 3.2 损失函数

### 3.2.1 判别器损失函数

![Equation 8](/images/201705/03/eq08.jpg)

![Equation 9](/images/201705/03/eq09.jpg)

### 3.2.2 Minimax 最小最大化

![Equation 10](/images/201705/03/eq10.jpg)

![Equation 11](/images/201705/03/eq11.jpg)

![Equation 12](/images/201705/03/eq12.jpg)


### 3.2.3 启发式， 非饱和游戏

![Equation 13](/images/201705/03/eq13.jpg)

### 3.2.4 最大似然游戏

![Equation 14](/images/201705/03/eq14.jpg)

### 3.2.5 

![Figure 14](/images/201705/03/fig14.jpg)

### 3.2.6 损失函数比较

## 3.3 DCGAN结构

## 3.4 



