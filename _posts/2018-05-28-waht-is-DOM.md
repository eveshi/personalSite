---
layout: post
title:  "图解DOM基础"
date:   2018-05-28 18:22:13 +0800
categories: basics
tag: 基础知识
---

DOM（Document_Object_Model）一直是网页学习中的一个重要概念。没有DOM，Javascript 等高级语言就无法对 HTML 等结构语言进行操作。

如下图所示，我们可以把 HTML 想象成一个学校，那么 Javascript 就是校长，DOM 则是教导主任。校长负责发号施令对全校进行一个调配，以向外界呈现一个最好的校园风貌。但是校长并不直接和同学们发生接触，而是通过教导主任 DOM 来进行具体的管理。

![图解DOM](https://raw.githubusercontent.com/eveshi/eveshi.github.io/master/assets/img/2018-05-28-DOM.PNG)

而对班级、同学的安排，对应到 DOM 中即是对于节点的操作。在 DOM 中，节点主要分为以下几种类型。

- 元素节点
- 属性节点
- 文本节点
- 注释节点
- 文档节点
- 文档类型节点
- 文档片段节点