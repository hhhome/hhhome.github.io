---
layout: post
title: Git 常用操作
description: "git operate"
tags: [sample post]
image:
  feature: abstract-10.jpg
---


{% highlight hmtl %}
添加文件  git add . // add all 
git add \\*.txt  // add all txt file


{% endhighlight %}

同步远程仓库代码到本地
git pull相当于是从远程获取最新版本并merge到本地。
{% highlight hmtl %}

git pull https://github.com/name.git

{% endhighlight %}
<!--more-->

同步本地代码到远程仓库
{% highlight hmtl %}

git push <remote name> <branch name> 
eg: git remote add origin https://github.com/name.git
	git push origin master

{% endhighlight %}

