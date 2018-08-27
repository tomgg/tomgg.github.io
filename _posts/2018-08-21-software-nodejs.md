---
layout: post
title: CentOS下安装nodejs
tags:  [软件,nodejs]
categories: [软件安装]
author: tomgg
excerpt: "CentOS下 nodejs 安装 教程 CentOS下 nodejs 安装 教程 CentOS下 nodejs 安装 教程 CentOS下 nodejs 安装 教程"
---


## 安装

### 步骤1：确认操作系统版本

``` shell
[root@csv-zdhc08 ~]# uname -a
Linux csv-zdhc08 3.10.0-327.el7.x86_64 #1 SMP Thu Nov 19 22:10:57 UTC 2015 x86_64 x86_64 x86_64 GNU/Linux
```
确认了操作系统是 64位 Linux

### 步骤2：软件下载

下载地址：https://nodejs.org/en/download/
![nodejs-web][1]

### 步骤3：上传软件

把下载下来的软件包 node-v8.11.4-linux-x64.tar.xz 上传到安装主机

### 步骤4：解压安装

``` shell
tar -xvf  node-v8.11.4-linux-x64.tar.xz
mv node-v8.11.4-linux-x64  node-v8.11.4
```




[1]: /assets/images/posts/2018-08-21-software-nodejs/01-nodejs-web.jpg "nodejs-web"
