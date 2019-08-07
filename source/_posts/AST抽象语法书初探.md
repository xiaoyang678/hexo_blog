---
title: AST抽象语法书初探
date: 2019-08-05 11:36:36
tags: [AST, javascript]
categories: "AST"
---

## 什么是AST
<!-- more -->
如果你查看目前任何主流的项目中的devDependencies，会发现前些年的不计其数的插件诞生。我们归纳一下有：javascript转译、代码压缩、
css预处理器、elint、pretiier，等。有很多js模块我们不会在生产环境用到，但是它们在我们的开发过程中充当着重要的角色。所有的上述工
具，不管怎样，都建立在了AST这个巨人的肩膀上。
> It is a hierarchical program representation that presents source code structure according to the grammar of a programming language, each AST node corresponds to an item of a source code.

以上是官方对AST(抽象语法树)给出的定义，

## 项目中使用AST

之前也在一些博客文章中提到了，一直没有去深入了解下，什么是ast，ast能实现什么。正好最近项目要有个需求，需要遍历所有代码中的catch代码，并在catch代码块中，注入一段日志收集脚本。当时拿到这个需求的时候，脑海中第一个反应就是使用正则匹配，然后替换代码。</br>
等真正开始做的时候，发现，自己根本不会正则，网上很难找到满足需求的正则表达式。哈哈。然后就不要脸的发了个帖子，网友推荐了babel插件，我们项目上是用gulp来做的代码编译，就准本分析下这个babel插件看下，怎么实现的，可以自己写一个gulp插件去实现下。分析下来，发现babel插件是通过ast去实现对js代码的处理。
