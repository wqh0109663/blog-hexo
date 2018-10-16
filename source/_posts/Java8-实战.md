---
title: Java8 实战
date: 2018-09-20 08:05:00
tags:
  - Java8
  - Lambda
categories: Java
---

## 牛客网的面试题
### 题目  
![](https://github.com/wqh0109663/MyOwnMarkDownPhoto/raw/master/Java8/niuke.png)

### 解析
```Java
/**
 * @author wqh
 * @date 18-9-21
 */
public class Son extends Father {
    public Son() {
        System.out.println("子类构造器");
    }

    static {
        System.out.println("子类静态代码块");
    }
    {
        System.out.println("子类代码块");
    }
    int c = 10 ;
    static int d = getB() ;

    public static void main(String[] args) {
        Son son = new Son();
    }
    public static  int getB(){
        System.out.println("子类静态变量初始化");
        return 0;
    }

}


```
```java
/**
 * @author wqh
 * @date 18-9-21
 */
public class Father {
    public Father() {
        System.out.println("父类构造器");
    }
    static {
        System.out.println("父类静态代码块");
    }
    {
        System.out.println("父类代码块");
    }
    static int a = getA() ;
    int b = 9 ;
    public static  int getA(){
        System.out.println("父类静态变量初始化");
        return 0;
    }
}

```
### 运行main，结果
![](https://github.com/wqh0109663/MyOwnMarkDownPhoto/raw/master/Java8/out.png)


## 待解决的问题

### java中io流的问题

### java中集合框架问题

### java中泛型问题
### 本质是参数化类型的应用
### 官网教程  

   * [官网地址](http://cr.openjdk.java.net/~briangoetz/lambda/lambda-state-final.html)

### java中注解问题

### java中反射问题

### Java中异常

### java中枚举

### java中内部类问题

### java中线程问题



## java8书中第三章关于Lambda表达式

### 基本语法

  1. (parameters) -> expression
  2. (parameters) -> {statements;}
