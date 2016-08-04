---
layout: post
title: eclipse中tab健为4个空格的方法
tags:  [eclipse,开发工具]
categories: [开发工具]
author: Tomgg
excerpt: "设置eclipse中tab健为4个空格的方法，使代码在不同编辑器下展现的效果相同"
---


1. 点击 window->preference-,依次选择 General->Editors->Text Editors,选中右侧的 insert space for tabs;如下图所示，保存，第一步完成；
![space4tabs][1]

***

2. 点击 window->preference-,依次选择 java（或C++）->code style ->formatter,点击右侧的editor，选则左侧 tab policy的值为spaces only,确定，应用保存即可，如下图所示：
![spaceOnly][2]

***

3. 若出现应用Apply按钮为灰色的情况，需要回到上一步，点击new按钮，根据当前的样式重新生成一个新的样式并保存，重复第2步，编辑该样式即可，如下图：
![newProfile][3]


[1]: /assets/images/posts/2016-08-02-eclipse-tab-space/01-space4tabs.jpg "space4tabs"
[2]: /assets/images/posts/2016-08-02-eclipse-tab-space/02-spaceOnly.jpg "spaceOnly"
[3]: /assets/images/posts/2016-08-02-eclipse-tab-space/03-newProfile.jpg "newProfile"
