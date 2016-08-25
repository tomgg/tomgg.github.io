---
layout: post
title: 线程同步工具CountDownLatch
tags:  [Java,多线程]
categories: [Java开发]
author: tomgg
excerpt: "我们有的时候有这样的需求，多个线程同时工作时，其中几个线程可以随意并发执行，但是其中有一个线程必须等待其他线程工作完成后才能开始执行。例如：开启对多线程进行文件下载，下载完成后由一个统一的线程进行文件合并操作。"
---


## CountDownLatch
 CountDownLatch是JAVA提供在java.util.concurrent包下的一个辅助类，可以把它看成是一个计数器，其内部维护着一个count计数，只不过对这个计数器的操作都是原子操作，同时只能有一个线程去操作这个计数器，CountDownLatch通过构造函数传入一个初始计数值，调用者可以通过调用CounDownLatch对象的cutDown()方法，来使计数减1；如果调用对象上的await()方法，那么调用者就会一直阻塞在这里，直到别人通过cutDown方法，将计数减到0，才可以继续执行。

```java
public class CountDownLatchTest {

    public class DonwLoad implements Runnable {
        CountDownLatch cdl;

        public DonwLoad(CountDownLatch cdl) {
            this.cdl = cdl;
        }

        @Override
        public void run() {
            try {
                System.out.println(Thread.currentThread().getName() + " Download Done!");
            } finally {
                cdl.countDown();
            }
        }
    }

    public static void main(String[] args) {
        try {
            CountDownLatch countDownLatch = new CountDownLatch(10);
            DonwLoad donwLoad = new CountDownLatchTest().new DonwLoad(countDownLatch);
            for (int i = 0; i < 10; i++) {
                new Thread(donwLoad).start();
            }
            countDownLatch.await();
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        System.out.println(Thread.currentThread().getName() + " File Merge!");
    }
}
```

```
Thread-2 Download Done!
Thread-1 Download Done!
Thread-7 Download Done!
Thread-8 Download Done!
Thread-3 Download Done!
Thread-9 Download Done!
Thread-0 Download Done!
Thread-6 Download Done!
Thread-4 Download Done!
Thread-5 Download Done!
main File Merge!

```
