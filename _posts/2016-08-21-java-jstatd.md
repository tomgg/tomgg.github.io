---
layout: post
title: jstatd用法
tags:  [Java,工具,JVM]
categories: [JVM工具]
author: tomgg
excerpt: "jstatd是jvm的分析工具，可以用它来分析内存、cpu使用情况，通过分析来找到影响性能的问题点"
---

jstatd远程服务开启

### 独立进程方式

第一步创建文件 jstatd.java.policy

```shell
grant codebase "file:${java.home}/../lib/tools.jar" {
   permission java.security.AllPermission;
};
```

第二步启动jstatd

``` shell
jstatd -J-Djava.security.policy=./jstatd.java.policy  -J-Dcom.sun.management.jmxremote.port=8888  -J-Dcom.sun.management.jmxremote.ssl=false  -J-Dcom.sun.management.jmxremote.authenticate=false
```
