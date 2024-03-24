# 使用 axios 发送 HTTP 请求

## 介绍

[https://axios-http.com/zh/](https://axios-http.com/zh/)
axios 是一个基于 Promise 的 HTTP 客户端，可以用于浏览器和 Node.js。它具有简洁的 API，易于使用，并且支持拦截器、取消请求、自动转换响应数据等功能。

## 安装

使用 npm:

```
npm install axios
```

使用 bower:

```
bower install axios
```

使用 yarn:

```
yarn add axios
```

使用 jsDelivr CDN:

<script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>

使用 unpkg CDN:

<script src="https://unpkg.com/axios/dist/axios.min.js"></script>

直接使用 require 导入预构建的 CommonJS 模块（如果模块打包器无法自动解析它们）

```
const axios = require('axios/dist/browser/axios.cjs'); // browser
const axios = require('axios/dist/node/axios.cjs'); // node
```
