---
layout: post
title: LeetCode Practice
date: 2020-03-01 10:07:21.000000000 +09:00
---

#### Problem 1367

查找二叉树中的列表

思路在于从列表的头节点依次在二叉树的父节点到左右两个子节点依次对比值是否相等。需要注意的是，因为列表的头节点不一定从根节点开始，需要对二叉树的左右子节点进行重复迭代 

#### 面试04

二维数组边界判断

```java
//分别对一维是否为空和长度为0 以及二维是否为空或者长度为0进行判断
        if(matrix == null || matrix.length == 0){
            return false;
        }

        int m = matrix.length;
        if(matrix[0] == null){
            return false;
        }

        int n = matrix[0].length;
        if(n == 0){
            return false;
        }
```

#### 面试05

```python
python中没有string.contains()，可以使用string.find() == -1 或 substring (not) in string
```

