---
layout: post
title: CentOS下安装nodejs
tags:  [软件,nodejs]
categories: [软件安装]
author: tomgg
excerpt: "Node.js 是一个基于 Chrome V8 引擎的 JavaScript 运行环境。 
          Node.js 使用了一个事件驱动、非阻塞式 I/O 的模型，使其轻量又高效。 
          Node.js 的包管理器 npm，是全球最大的开源库生态系统。 "
---


## 安装

### 步骤1：确认操作系统版本

![os-version][2]

确认了操作系统是 64位 Linux

### 步骤2：软件下载

下载地址：[https://nodejs.org/en/download/](https://nodejs.org/en/download/)
![nodejs-web][1]

### 步骤3：上传软件

把下载下来的软件包 node-v8.11.4-linux-x64.tar.xz 上传到安装主机

### 步骤4：解压安装

``` shell
tar -xvf  node-v8.11.4-linux-x64.tar.xz
mv node-v8.11.4-linux-x64  node-v8.11.4
```

### 步骤5：创建链接

```shell
ln -s /software/nodejs/node-v8.11.4/bin/npm /usr/local/bin/
ln -s /software/nodejs/node-v8.11.4/bin/node /usr/local/bin/
```


[1]: /assets/images/posts/2018-08-21-software-nodejs/01-nodejs-web.jpg "nodejs-web"
[2]: /assets/images/posts/2018-08-21-software-nodejs/02-os-version.jpg "os-version"
