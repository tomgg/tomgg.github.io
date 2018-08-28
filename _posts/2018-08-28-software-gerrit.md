---
layout: post
title: CentOS下安装gerrit
tags:  [软件,gerrit]
categories: [软件安装]
author: tomgg
excerpt: "gerrit 代码托管工具，支持代码review，代码审核"
---



1、创建用户
```shell
useradd -m gerrit -d /software/gerrit  -g software
```

2、下载软件
https://www.gerritcodereview.com/
gerrit-2.15.3.war

3、上传软件

4、设置代理
```shell
export http_proxy=proxy.zj.chinamobile.com:8080
export https_proxy=proxy.zj.chinamobile.com:8080
```





