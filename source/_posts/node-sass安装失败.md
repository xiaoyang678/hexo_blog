---
title: node-sass安装失败
date: 2019-11-08 15:32:41
tags:
---

## node-sass安装失败，一般以下两种解决办法

* 我们一般更希望能跨平台、并且直接使用 npm install 安装所有依赖，所以我的做法是在项目内添加一个 .npmrc 文件：

```
sass_binary_site=https://npm.taobao.org/mirrors/node-sass/
phantomjs_cdnurl=https://npm.taobao.org/mirrors/phantomjs/
electron_mirror=https://npm.taobao.org/mirrors/electron/
registry=https://registry.npm.taobao.org
```
<!-- more -->
* 使用梯子

```
npm config set proxy http://127.0.0.1:1080
npm i node-sass

# 下载完成后删除 http 代理
npm config delete proxy
```