---
layout: post
title: jekyll introduction
description: "jekyll introduction"
tags: [sample post]
image:
  feature: abstract-3.jpg
---

jekyll是一个类似于WordPress简单的免费的Blog生成工具。与WordPress不同的是: jekyll是一个生成静态网页的工具，不需要数据库支持,可以配合第三方服务,实现各种功能，例如：
disqus评论系统 
jekyllg可以免费部署在Github上，而且可以绑定自己的域名。

jeykyll的优点
  1）默认支持markdown语法。
  2）本地文件操作，只要新建了一个文件，刷新一下，页面上就有了发布的文件，无所谓数据库之类的。


<!--more-->
jeykyll 标准目录树
_config.yml   Jekyll的配置文件
_includes     include 文件所在的文件夹
_layouts      模版文件夹
_posts        自己要发布的内容
_sites        预览时产生的文件都放在该文件夹中

jeykyll 模板全局变量

|| *变量* || *描述* || 
|| site || 全站的信息+_config.yml文件中的配置选项 || 
|| page || 这个变量中包含YAML前置数据,另外加上两个额外的变量值:url和content。 ||
|| content || 在布局模板文件中，这里变量包含了页面的子视图。这个变量将会把渲染后的内容插入到模板文件中。这个变量不能在文章和页面文件中使用。 ||
|| paginator || 一旦paginate配置选项被设置了，这个变量才能被使用。 ||