---
layout: post
title: 如何获得真随机数
tags:  [eclipse,开发工具]
categories: [开发工具]
author: Tomgg
excerpt: "设置eclipse中tab健为4个空格的方法，使代码在不同编辑器下展现的效果相同"
---

上一篇[如何获得随机数]({{ site.baseurl}}/2016/07/20/java-random/)


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
