---
layout: post
title: Git 常用操作
description: "git operate"
tags: [sample post]
image:
  feature: abstract-10.jpg
---



添加文件  git add . // add all 
git add \\*.txt  // add all txt file




同步远程仓库代码到本地
git pull相当于是从远程获取最新版本并merge到本地。


git pull https://github.com/name.git


<!--more-->

同步本地代码到远程仓库


git push <remote name> <branch name> 
eg: git remote add origin https://github.com/name.git
	git push origin master



