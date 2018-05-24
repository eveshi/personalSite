---
layout: post
title:  "一张图解释CDN"
date:   2018-02-23 12:21:42 +0800
categories: basics
tag: 基础知识
---

很多初学编程的朋友都对 CDN（Content Delivery Network）（内容分发网络）的运行机制有一定疑问。

其实简单来说 CDN 就是通过增加 Edge Server 的方式，让用户在访问互联网的过程中，尽可能的使用本地或就近的服务器，尽可能利用缓存，来节省重复、冗余数据传输成本。

下图就是一个典型的 CDN 场景。

![图解cdn]({{site.url}}/assets/img/2018-02-23-CDN.PNG)

按照图例，在开发者将内容发布之后（图中例子是发布到 heroku.com 上），用户访问网站数据会遵循以下步骤：
1. 向 DNS Server 发送请求，获取 Edge Server 的 IP 地址。
2. 向 Edge Server 发送请求，其中：
    - 若 Edge Server 中不包含网站缓存，则先向 Origin Server 发送请求，获取网站数据。
    - 若已包含网站缓存，则：
        -  下载数据到浏览器。（若首次下载，下载全部内容；若本地已有缓存，则下载缓存之外的部分）

