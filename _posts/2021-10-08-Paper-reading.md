---
title: 论文阅读（2021.9.28-2021.10.9）
tags: Paper
key: key_32
pageview: true
---

高维训练向量集合：$I={x_i}$；对于$I$中的每条样本${x_i}$，$S_{x_i}$表示与$x_i$相似的样本集合；$y = 0$表示$x_1$与$x_2$相似；$y = 1$表示$x_1$与$x_2$不相似；$D_W ( x 1 , x 2 )$表示$G_W$输出间的欧氏距离：

$$
D_W(x_1, x_2) = ||G_W(x_1) − G_W(x_2)||_2
$$ 

则对比损失函数定义为：

$$
L(W) = \sum_{i=1}^PL(W, ( y , x_1 , x_2)^i) 
$$

$$
L(W, ( y , x_1 , x_2)^i) = (1 - y)L_s(D^i_W) + yL_D(D^i_W)
$$

其中:

$(y, x_1, x_2)^i$ 为第 $i$ 对标记样本

$L_S$为相似样本间部分损失函数（partial loss function for a pair of similar points）

$L_D$为非相似样本间部分损失函数（partial loss function for a pair of dissimilar points）

$P$为样本对总数