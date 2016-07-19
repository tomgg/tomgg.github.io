---
layout: post
title: Java Socket 编程
tags:  [Java]
categories: [Java]
author: tomgg
excerpt: "Java Socket 编程"
---


## Socket 服务端创建
```java
	public void startThreadUseSubClass() {
		class MyThread extends Thread {
			public void run() {
				System.out.println("start thread using Subclass of Thread");
			}
		}

		MyThread thread = new MyThread();
		thread.start();
	}
```