---
layout: post
title: 如何创建一个线程
tags:  [Java,多线程]
categories: [Java开发]
author: tomgg
excerpt: "按 Java 语言规范中的说法，创建线程只有一种方式，就是创建一个 Thread 对象。而从 HotSpot 虚拟机的角度看，创建一个虚拟机线程
有两种方式，一种是创建 Thread 对象，另一种是创建 一个本地线程，加入到虚拟机线程中。"
---

##安装

步骤1：确认操作系统版本
``` shell
[root@csv-zdhc08 ~]# uname -a
Linux csv-zdhc08 3.10.0-327.el7.x86_64 #1 SMP Thu Nov 19 22:10:57 UTC 2015 x86_64 x86_64 x86_64 GNU/Linux
```
确认了操作系统是64位Linux

步骤2：软件下载
下载地址：https://nodejs.org/en/download/

![nodejs-web][1]



[1]: /assets/images/posts/2018-08-21-software-nodejs/01-nodejs-web.jpg "nodejs-web"
