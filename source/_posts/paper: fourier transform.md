---
title: 论文阅读：fourier transform
date: 2021-07-12 15:09:30
tags: Paper
img: /images/blackboard.jpg
mathjax: true

---

## 图像中的傅里叶变换

[重要参考博客](https://www.cnblogs.com/wj-1314/p/11983496.html#:~:text=%E4%BB%8E%E7%BA%AF%E7%B2%B9%E7%9A%84%E6%95%B0%E5%AD%A6%E6%84%8F%E4%B9%89,%E5%9B%BE%E5%83%8F%E7%9A%84%E9%A2%91%E7%8E%87%E5%88%86%E5%B8%83%E5%87%BD%E6%95%B0%E3%80%82)

> 图像的频率是表征图像中灰度变换剧烈程度的指标，是灰度在平面空间上的梯度。如：大面积的沙漠在图像中是一片灰度变化缓慢的区域，对应的频率值很低；而对于地表属性变换剧烈的边缘区域在图像中是一片灰度变化剧烈的区域，对应的频率值较高。傅里叶变换在实际中有明显的物理意义，设f 是一个能量有限的模拟信号，则其傅里叶变换就表示 f 的频谱。从纯粹的数学意义上看，傅里叶变换是将一个函数转换为一系列周期函数来处理的。从物理效果来看，傅里叶变换是将图像从空间域转换到频率域，其逆变换是将图像从频率域转换到空间域。换句话说，傅里叶变换的物理意义是将图像的灰度分布函数变换为图像的频率分布函数。

图像变化剧烈则福利也变化频率高，反之则低。

## 启发
把傅里叶变换用到graph上，相邻节点的representation应该相似，对应傅里叶变换上应该低频。

所以可以在graph上做傅里叶变换，然后做低通，高频的被去掉了，因为它们很可能是label noise。

