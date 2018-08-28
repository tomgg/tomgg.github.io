---
layout: post
title: CentOS下安装Gerrit
tags:  [软件,gerrit]
categories: [软件安装]
author: tomgg
excerpt: "Gerrit，一种免费、开放源代码的代码审查软件，使用网页界面。利用网页浏览器，同一个团队的软件程序员，可以相互审阅彼此修改后的程序代码，决定是否能够提交，退回或者继续修改。"
---


 

1、创建用户

```shell
useradd -m gerrit -d /software/gerrit  -g software
```
gerrit\1q2w3e4r@20.26.39.26

2、下载软件

https://www.gerritcodereview.com/

gerrit-2.15.3.war

3、上传软件

4、设置代理

```shell
export http_proxy=proxy.zj.chinamobile.com:8080
export https_proxy=proxy.zj.chinamobile.com:8080
```

5、数据库
```
IP：20.26.26.27 
PORT:3306
DBName： reviewdb 
用户名：gerrit
密码：gerrit123
```

参考：[URL]https://www.wolfcstech.com/2017/11/24/gerrit_codereview/





