---
title: Java基于Springboot+gradle编写文件处理脚本
date: 2019/1/31
permalink: file
categories: blog/java
tags: [java,Blog]
description: Java基于Springboot+gradle编写文件处理脚本

---

## 前言
最近接到一个需求，要将一批多层次文件夹里面的文件根据其中某一层合并为一个个PDF文件，并将文件上传到固定的服务器上，要求处理的文件包括ppt，excel，word以及各种图片格式，其中图片格式要求压缩。
因为只是脚本，所以基于最基础的Springboot+gradle来构建框架。
应用到的主要技术有：
1. office文件转pdf________________________aspose
2. 图片压缩________________________等宽压缩（实测显示效果比较好，但是压缩大小不是很理想。需求相反的话推荐用Thumbnails）
3. 图片转pdf________________________itext
4. pdf合成________________________itext
5. 图片格式转化（部分图片格式用itext转pdf会报错，先转化为其他格式再转pdf）________________________jai 
6. 读取excel文件________________________poi
7. 上传文件________________________httpclient
8. 输出csv文件________________________csv  
