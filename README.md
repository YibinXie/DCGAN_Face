# DCGAN_Face
## 介绍

DCGAN将深度卷积神经网络（CNN）与生成对抗网络（GAN）相结合。DCGAN是对Goodfellow在2014年提出的原始GAN网络的一种改进。主要包括以下几个方面：

- 使用卷积层代替池化层
- 生成器和判别器都是用BN
- 移除全连接层
- 生成器除了输出层使用Tanh外，其他层均使用ReLU作为激活函数
- 判别器除了输出成使用sigmoid外，其他层均使用LeakyReLU作为激活函数

DCGAN的生成器部分如下图所示：

![Illustrating the architecture of DCGAN](/figures/DCGAN.png)

虽然DCGAN的论文中并没有给出判别器的结构图，但是从文中的描述可以知道判别器同样也是5层的网络结构。



结果分析

## 总结

GAN是比较难训练的，通过实验发现，仅仅是修改一些超参数或是激活函数都有可能是网络生成的图像为噪声或者出现mode collapse现象。实现GAN网络不仅要考虑网络结构，还要考虑损失函数的优化过程，生成器和判别器要相当。

