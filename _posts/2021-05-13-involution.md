---
title: 论文笔记-Involution Inverting the Inherence of Convolution for Visual Recognition
tags: Paper-reading
key: key_13
pageview: true
---

## 论文贡献

1、提出新的网络算子Involution

2、从Involution角度统一Convolution和Attention


## Convolution的两大特性

1、空间不变性(Spatial-agnostic)

在H×W的像素空间共享相同的kernel

2、通道特异性(channel-specific)

每个通道独享对应的kernel


## Involution特性

在通道维度共享kernel，在空间维度采用空间特异的kernel进行建模

involution kernel 大小: H × W × K × K × G.

其中，G << C，表示所有通道共享kernel的数量。

## 伪代码

![pseudo code](/assets/images/blog/involution_pseudo_code.png)

## 参考文献

[Involution: Inverting the Inherence of Convolution for Visual Recognition](https://arxiv.org/pdf/2103.06255.pdf)
