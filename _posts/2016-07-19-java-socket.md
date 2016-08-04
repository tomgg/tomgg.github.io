---
layout: post
title: Java Socket 编程
tags:  [Java,Socket]
categories: [Java开发]
author: tomgg
excerpt: "Java Socket 编程  Socket 服务端创建 Socket 服务端创建 Socket 服务端创建 Socket 服务端创建"
---


## Socket 服务端创建
```java
	public class SocketServer {

	public static void main(String[] args) {
		try {
			ServerSocket server = new ServerSocket(10010);
			while (true) {
				Socket socket = server.accept();
				invoke(socket);
			}
		} catch (Exception e) {
			e.printStackTrace();
		}
	}

	private static void invoke(final Socket client) throws IOException {
		new Thread(new Runnable() {
			public void run() {
				BufferedReader in = null;
				PrintWriter out = null;
				try {
					in = new BufferedReader(new InputStreamReader(
							client.getInputStream()));
					out = new PrintWriter(client.getOutputStream());

					while (true) {
						String msg = in.readLine();
						System.out.println(msg);
						out.println("Server received " + msg);
						out.flush();
						if (msg.equals("bye")) {
							break;
						}
					}
				} catch (IOException ex) {
					ex.printStackTrace();
				} finally {
					try {
						in.close();
					} catch (Exception e) {
					}
					try {
						out.close();
					} catch (Exception e) {
					}
					try {
						client.close();
					} catch (Exception e) {
					}
				}
			}
		}).start();
	}
}
```
