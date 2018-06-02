---
layout: post
title:  "数据新闻网项目总结"
date:   2018-06-02 20:41:06 +0800
categories: react
tag: React
---

数据新闻网这个项目是一个 single-page website。这个项目整体使用了 React.js + Express.js + MongoDB 的架构。

MongoDB 采用了用户表，课程表和论坛表三个主表。之后会考虑把评论单独拉出来，在评论量较大时，会在获取数据方面更方便。

用户登录的管理使用了 Redux。在用户界面，用户也可以实时更改头像、昵称密码等。密码找回使用了验证码+邮箱的形式。发送邮件采用了 nodemailer 这个库。图片验证码使用了 session + captchapng 的方法生成图片验证码。

在线课程部分，用户可以进行评论以及收藏和点赞。视频的处理使用了 youtube 本身的 API 。论坛也可以进行发帖和评论。所有的贴文处理都是用了 Markdown 的方式，而没有采用富文本。

整个网站的 CSS 都采用 CSS module。因为阅读会非常方便，使用简介，解决了很多诸如全局命名的问题。

点击查看[项目](https://github.com/eveshi/data-journalism)
点击查看[测试网页](https://data-journalism.herokuapp.com/)