---
title: gulp 使用体验
date: 2019-06-21 10:56:38
tags: [gulp, 体验]
categories: "体验"
---
## 什么是gulp

个人理解gulp和webpack对比下来，gulp是一个轻量级的前端构建工具，下面摘抄别人博客对gulp的介绍
<!-- more -->
> gulpjs是一个前端构建工具，与gruntjs相比，gulpjs无需写一大堆繁杂的配置参数，API也非常简单，学习起来很容易，而且gulpjs使用的是nodejs中stream来读取和操作数据，其速度更快。如果你还没有使用过前端构建工具，或者觉得gruntjs太难用的话，那就尝试一下gulp吧
官网地址 https://www.gulpjs.com.cn/ ,现在gulp和webpack的官方文档很大一部分都已经中文化了，总的来说，gulp使用起来比webpack更加的简单，也更加的自由。有兴趣可以看下gulp的插件的源码，代码量都不是很多。

在使用gulp对老项目的代码进行打包的过程中，发现自身项目中有一个需求【每次发包前需要对项目代码中对一个xml文件进行一个格式内容对检查】,一开始看到处理这个的时候，脑海中第一个想法就是能不能通过gulp插件来实现尼，这样的话就可以很简单的通过多个task串行完成了。那么这种插件肯定是一种定制化了，就找了使用到的gulp-zip插件的源码来看一下了，发现源码很少，代码也很简单了。

然后就自己手动写一个gulp插件来实现功能了。
