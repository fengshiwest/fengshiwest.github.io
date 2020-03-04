---
layout: post
title: Algorithm And Machine Learning
date: 2020-03-04 10:07:21.000000000 +09:00
---

### 算法与机器学习

![1583280896696](C:\Users\west\Desktop\fengshiwest.github.io\_posts\img\AlgorithmAndMachineLearningMind.png)

计算平方根（牛顿迭代法）

```java
public static double sqrt(double c){
    if(c < 0)
        return Double.NaN;
    double err = 1e-15;  //精度控制在10^(-15)内
    double t = c;
    while(Math.abs(t - c/t) > err * t)
        r = (c/t + t) / 2.0;
    return t;
}
```



重定向与管道：突破能够处理的输入输出流的长度限制

```java
输出：java RandomSeq 1000 100.0 200.0 > data.txt
输入：java Average < data.txt
管道：java RandomSeq 1000 100.0 200.0 | java Average
```



二分查找 Binary Search

```java
public static int rank(int key, int[] a){
    int low = 0;
    int high = a.length - 1;
    while(low <= high){
        int mid = low + (high - low) / 2;
        if(key < a[mid])
            high = mid - 1;
        else if(key > a[mid])
            low = mid + 1;
        else
            return mid;
    }
    return -1;
}
```

