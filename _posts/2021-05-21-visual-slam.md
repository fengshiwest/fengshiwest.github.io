---
title: 视觉SLAM十四讲5
tags: book-reading
key: key_1
pageview: true
---

## 一、概述

SLAM(Simultaneous Localization and Mapping)，同时定位与地图构建。指搭载特定传感器的主体，在没有环境先验信息的情况下，于运动中建立环境的模型，同时估计自己的运动。

## 二、SLAM框架

1、**传感器信息读取**。相机图像信息读取与预处理。

2、**前端视觉里程计**（Visual Odometry）。估算相邻图像间相机的运动，以及局部地图的样子。

3、**后端（非线性）优化**。接受不同时刻视觉里程计测量的相机位姿，以及回环检测的信息，对它们进行优化，得到全局一致的轨迹和地图。

4、**回环检测**。判断机器人是否到达过先前的位置，如果检测到回环，会把信息提供给后端处理。

5、**建图**。根据估计的轨迹，建立与任务要求对应的地图。

## 三、三维空间刚体运动

欧氏空间坐标变化：旋转矩阵 R + 平移向量 t.

$$
a^{\prime} = Ra+t
$$

转化为齐次坐标和变换矩阵形式：

$$
\begin{bmatrix}
a^{\prime }
\\
1
\end{bmatrix}
=
\begin{bmatrix}
 R & t\\
 0^{T} & 1
\end{bmatrix}
\begin{bmatrix}
a
\\
1
\end{bmatrix}
= T \begin{bmatrix}
a
\\
1
\end{bmatrix}
$$

