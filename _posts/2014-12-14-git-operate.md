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
{% raw %}

git pull https://github.com/name.git

{% endraw %}

{% raw %}

git fetch origin master  //从远程的origin的master主分支下载最新的版本到origin/master分支    

git log -p master..origin/master  //比较本地的master分支和origin/master分支的差别    

git merge origin/master  //合并到本地   


{% endraw %}

{% raw %}

git fetch origin master:tmp    

git diff tmp     

git merge tmp  

{% endraw %}


<!--more-->

同步本地代码到远程仓库

{% raw %}

git push <remote name> <branch name> 
eg: git remote add origin https://github.com/name.git
	git push origin master

{% endraw %}



