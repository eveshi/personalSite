---
layout: post
title:  "React新手常见问题总结"
date:   2018-05-30 16:44:22 +0800
categories: react
tag: React
---
这里总结了一些 React 以及新手常见错误。后续也将不断更新。

1. Import某一模块后，出现错误提示如下：
    ```
    Critical dependency: the request of a dependency is an expression.
    ```

    出现这一个提示的时候请检查自己文件中的import：
    - 是否是格式错误。
    - 是否是import的模块和本身的环境并不兼容。（比如本来不是 React 的模块在 React 中进行了使用。）

2. 使用 axios 传参，后台无法接收：
    文件上传时，服务器都进行了特殊处理，在解析时，需要知道处理方式才能正确解析数据。而使用原生 ajax 请求时，如果不设置 Content-Type，那么就会使用默认默认的 text/plain，这时，服务器只能通过获取原始数据流的方式来解析请求数据，便与真正方式不符、无法拿到正确数据了。简单来说，就是需要把 post 传的参数进行序列化。以及需要重申content-type。可加入一个包装 axios 的文件如下：

    ```js
    import axios from 'axios';
    import Qs from 'qs';

    const instance = axios.create({
        baseURL: __dirname,
        headers: {"Content-Type": "application/x-www-form-urlencoded"},
        transformRequest: [function (data) { data = Qs.stringify(data); return data }]
    })

    export default instance;
    ```

    然后在使用时，import 该文件 export 的 axios 即可。

