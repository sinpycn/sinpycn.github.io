
20.10.3 Variational Autoencoders

The variational autoencoder or VAE (Kingma, 2013; Rezende et al., 2014) is a directed model that 
     uses learned approximate inference 
     and can be trained purely with gradient-based methods.


Adversarial Autoencoders

25th, May, 2016

Abstarct
AAE is a probabilistic autoencoder uses
  GAN to perform variational inference 
    by matching the aggregatd posterior of the hidden code vector of the autoencoder with an arbitrary prior distribution.    
    Matching the aggregated posterior to the prior ensures that generating from any part of prior space results in meaningful samples.
    As a result, the decoder of the AAE learns a deep generative model that maps the imposed prior to the data distribution.

AAE 是一个概率性自动编码器， 使用GAN来进行变分预测： 
    通过将自动编码器的z的先验的和，与一个辅助的后验分布对应。 
    此对应保证了产生来自任何先验空间，导致有意义的样本。
结果是： AAE的解码器，学习一个深度生成模型， 将强制先验映射到数据分布上。

Introduction

In this model, an autoencoder is trained with dual objectives:
    1. A traditonal reconstruction error criterion
    2. An adversarial training criterion (matches the aggregated posterior distribution of the latent representation of the autoencoder to an arbitrary prior distribution)
    
    this training criterion has a strong connection to VAE training.


