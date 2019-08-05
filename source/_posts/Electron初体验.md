---
title: Electron初体验
date: 2019-01-28 09:32:02
tags: [Electron, 体验]
categories: "体验"
---

### 前言

Electron出来已经很久了，vscode也是基于Electron实现了，之前老早就想说写个Electrondemo玩下。终于年前空闲有空看看了。

![](D:\03 coding\gayhub\hexo_blog\source\_posts\Electron初体验\img1.png)
<!-- more -->
### 安装

安装很简单就是跟着官方文档 npm i electron 就好了，不过过程中有个报错

```shell
Downloading tmp-3324-0-electron-v4.0.2-win32-x64.zip
Error: read ECONNRESET
```

大概就是下载这个文件有异常，设置了代理就可以了<code> npm config set ELECTRON_MIRROR "https://npm.taobao.org/mirrors/electron/"</code>  具体的可以参考<a href="https://github.com/electron-userland/electron-packager/issues/699">这个issues</a> 

### 文档

<a href="https://electronjs.org/docs">官方文档</a> 
