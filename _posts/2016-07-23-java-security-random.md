---
layout: post
title: 如何获得真随机数
tags:  [Java,Random,Security]
categories: [Java]
author: Tomgg
excerpt: "上一篇如何获得随机数中介绍JAVA语言中常用的随机数的获取方式，但是由于这些方式获取的都是伪随机数，在一些对安全性要求较高的场景上会有一点的风险,本文将介绍如何获得安全性较高的随机数。"
---

上一篇[如何获得随机数]({{ site.baseurl}}/2016/07/20/java-random/)中介绍JAVA语言中常用的随机数的获取方式，但是由于这些方式获取的都是伪随机数，在一些对安全性要求较高的场景上会有一点的风险。


1、打开security的debug log
-Djava.security.debug=all
安全的随机数
1、随机数加密
  加密算法获取
2、随机数种子
    计算机熵

    熵的获取
    配置
    使用


+ #### java.security.SecureRandom

SecureRandom的实现由两点要求
1、随机数的种子必须是不可预知的
2、随机数的输出序列必须是经过加密算法加密的
