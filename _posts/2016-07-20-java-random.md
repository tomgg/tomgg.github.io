---
layout: post
title: 如何获取随机数
tags:  [Java]
categories: [Java]
author: Tomgg
excerpt: "随机数的特征，随机数的种类，不同种类的应用场景，java中如何获取随机数，真正随机数如何获取？"
---


#### 随机数介绍
**随机数特征**
1. 该数字的出现是不可预知的。
2. 多个数时，数字和数字之间毫无关系。

**真随机数**
真正的随机数是使用物理现象产生的：比如掷钱币、骰子、转轮、使用电子元件的噪音、核裂变等等。这样的随机数发生器叫做物理性随机数发生器，产生的数字就是真随机数。它们的缺点是技术要求比较高。

**伪随机数**
在实际应用中往往使用伪随机数就足够了。这些数列是“似乎”随机的数，实际上它们是通过一个固定的、可以重复的计算方法产生的。计算机或计算器产生的随机数有很长的周期性。它们不真正地随机，因为它们实际上是可以计算出来的，但是它们具有类似于随机数的统计特征。这样的发生器叫做伪随机数发生器，产生的数字就是伪随机数。

>在真正关键性的应用中，比如在密码学中，人们一般使用真正的随机数。

C语言、C++、C#、Java、Matlab等程序语言和软件中都有对应的随机数生成函数，如rand等。

#### 随机数获取
**伪随机数**
Java中随机数的获取有多种方式
1. java.util.Random类
Random类中实现的随机算法是伪随机，也就是有规则的随机。在进行随机时，随机算法的起源数字称为种子数(seed)，在种子数的基础上进行一定的变换，从而产生需要的随机。


Random的构造方法

有参的

``` java
public static Random random4seed = new Random(10);
```

该方法可以通过一个种子数进行创建。
>注意：种子数是随机算法的起源数，和生成随机数的区间无关。
相同种子数的Random对象，相同次数生成的随机数字是完全相同的。

示例1代码

``` java
public class RandowGen {
	public static Random random = new Random(10);
	public static Random random2 = new Random(10);

	public static void main(String[] args) {
		for (int i = 0; i < 5; i++) {
			System.out.println("random  第"+(i+1)+"次结果:"+random.nextInt());
			System.out.println("random2 第"+(i+1)+"次结果:"+random2.nextInt());
		}
	}
}
```

示例1结果

``` 
random  第1次结果:-1157793070
random2 第1次结果:-1157793070
random  第2次结果:1913984760
random2 第2次结果:1913984760
random  第3次结果:1107254586
random2 第3次结果:1107254586
random  第4次结果:1773446580
random2 第4次结果:1773446580
random  第5次结果:254270492
random2 第5次结果:254270492
```

无参数

``` java
public static Random random = new Random();
```

实际上该方法内部会拿一个数和系统当前纳秒时间做一个异或操作的结果作为种子数，再调用有参的构造方法。
由于系统时间是一直在变化的，基本上得到随机数很难重复。

Random的成员方法








2. java.lang.Math


``` java	
public static float genRandomNum(long l) {
		return new Random(l).nextFloat();
	}
```



**真随机数**
熵池
java.util.Random
java.security.SecureRandom