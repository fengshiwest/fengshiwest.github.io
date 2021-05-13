---
title: CNN可视化
tags: 
key: key_7
pageview: true
---

## 论文笔记: Visualizing and Understanding Convolutional Networks

### 本文贡献

1. 介绍了一种可视化技术，揭示了在模型的任意层激发单独特征映射的输入促进因素。
2. 在训练过程中观察特征的演变，并诊断模型的潜在问题。我们提出的可视化技术使用多层反卷积网络(deconvnet)将特征激活投影回输入像素空间。
3. 对分类器输出进行灵敏度分析，通过遮挡输入图像的部分，揭示场景的哪些部分对分类是重要的。

## 论文笔记：Deep Inside Convolutional Networks: Visualising Image Classification Models and Saliency Maps

### 本文贡献

1. 提出显著性图(Saliency Maps)


### 显著性图原理

计算每一个像素点的导数，表示该点的微小改变对于结果的影响程度，从而看可以得知该像素点对于图像分类结果的影响。

### 代码实现

[Saliency Maps ipynb](https://github.com/wmn7/ML_Practice/blob/master/2019_07_08/Saliency%20Maps/Saliency%20Maps%20Picture.ipynb)


## CNN Explainer

[演示地址](https://poloclub.github.io/cnn-explainer/)

[Github](https://github.com/poloclub/cnn-explainer)

## 对CNN各层作用的理解

### 输入层

对于RGB图像，输入层有R、G、B三个通道；对于灰度图像，输入层只有单通道。

### 卷积层

参数：

Padding: 补充图像的边缘部分，一般补0

Kernel Size: 卷积核大小

Stride: 卷积核滑动步长

### 激活函数

ReLU: 增加模型的非线性

（什么是非线性？一阶导数非常数，虽然ReLU在大于0和小于0部分均为线性，但是组合起来为非线性。）

Softmax: 使CNN的输出之和为1

### 池化层

减少网络空间范围，从而降低网络的参数和计算量

## 激活层可视化

[项目地址](https://yosinski.com/deepvis)


## 参考文献

[1] Jason Yosinski, Jeff Clune, Anh Nguyen, Thomas Fuchs, and Hod Lipson. Understanding neural networks through deep visualization. Presented at the Deep Learning Workshop, International Conference on Machine Learning (ICML), 2015.
