---
layout: post
title:  "项目架构改动的一点思考"
date:   2018-03-22 19:23:12 +0800
categories: react
tag: React
---

在做一个 single-page-react-project 的过程中，我将项目结构进行了如下改动：

![react-architecture](https://raw.githubusercontent.com/eveshi/eveshi.github.io/master/assets/img/2018-03-22-react-architecture.PNGs)

也就说是把原本放到 client 文件夹中的内容全部提了出来。

两种结构各有利弊，第一种，将 server 和 client 进行了清晰的功能区分，但是层级较多；第二种则内容一目了然。

自我感觉，前者更适合于初学者，需要明确知道自己在动作的部分，而总体来说，后者对于项目的整体把控却是更高的。