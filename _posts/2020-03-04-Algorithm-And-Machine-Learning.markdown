---
layout: post
title: Algorithm And Machine Learning
date: 2020-03-04 10:07:21.000000000 +09:00
---

### 算法与机器学习

![1583280896696](C:\Users\west\Desktop\fengshiwest.github.io\_posts\img\AlgorithmAndMachineLearningMind.png)

#### 计算平方根（牛顿迭代法）

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



#### 重定向与管道：

突破能够处理的输入输出流的长度限制

```java
输出：java RandomSeq 1000 100.0 200.0 > data.txt
输入：java Average < data.txt
管道：java RandomSeq 1000 100.0 200.0 | java Average
```



#### 二分查找 Binary Search

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



#### 使用new创建对象包括：

1. 为新的对象分配内存空间
2. 调用构造函数初始化对象中值
3. 返回该对象中的一个引用



#### 构造函数

每个类都至少含有一个构造函数来创建一个对象的标识 用于初始化实例变量



#### 封装的优点

1. 独立开发用例和实现的代码
2. 切换至改进的实现而不会影响用例的代码
3. 支持尚未编写的程序



#### 接口

定义子类来继承父类的所有实例方法和实例变量

子类可以重新定义或者重写父类的方法



#### Java垃圾回收

Java不允许修改引用，使得能够高效回收垃圾

通过记录孤儿对象（引用被赋值语句覆盖）并将它们的内存释放到内存池中



#### 实现栈（动态调整数组大小）

```java
public class ResizingArrayStack<Item> implements Iterable<Item> {
    private Item[] a = (Item[]) new Object[1];
    private int N = 0;
    public boolean isEmpty(){
        return N == 0;
    }
    public int size(){
        return N;
    }
    
    //将栈移动到一个大小为max的数组
    private void resize(int max){
        Item[] temp = (Item[]) new Object[max];
        for(int i = 0; i < N; i++){
            temp[i]  = a[i];
        }
        a = temp;
    }
    
    //入栈
    public void push(Item item){
        if(N == a.length){
            resize(2 * a.length);
            a[N++] = item;
        }
    }
    
    //出栈
    public Item pop(){
        Item item = a[--N];
        a[N] = null;
        if(N > 0 && N == a.length/4){
            resize(a.length/2);
        }
        return item;
    }
    
    public Iterator<Item> iterator(){
        return new ReverseArrayIterator();
    }
    private class ReverseArrayIterator implements Iterator<Item>{
        private int i = N;
        public boolean hasNext(){
            return i > 0;
        }
        public Item next(){
            return a[--i];
        }
        public void remove(){
            
        }   
    }  
}
```

