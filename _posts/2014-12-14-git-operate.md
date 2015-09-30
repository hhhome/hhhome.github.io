---
layout: post
title: Git 常用操作
description: "git operate"
tags: [sample post]
image:
  feature: abstract-10.jpg
---



添加文件   
{% raw %}
	git add . // add all   

	git add \\*.txt  // add all txt file  

{% endraw %}

同步远程仓库代码到本地  

git pull相当于是从远程获取最新版本并merge到本地。  

{% raw %}

	git pull https://github.com/name.git

{% endraw %}

 git fetch：相当于是从远程获取最新版本到本地，不会自动merge  
 
{% raw %}

	git fetch origin master            //从远程的origin的master主分支下载最新的版本到origin/master分支    

	git log -p master..origin/master   //比较本地的master分支和origin/master分支的差别    

	git merge origin/master            //合并到本地   


{% endraw %}
上述过程其实可以用以下代码来代替，
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

查看记录
{% raw %}
	git log -p <file> //查看每次详细修改

	git log -p -2 //查看最近两次详细修改

	git log --stat //查看提交统计信息
{% endraw %}

删除空目录
使用git rm -rf dir 命令删除非空目录之后，本地还是会有空的目录存在，这时候空目录已经是untracked状态了
然后 再删掉 untracked状态的目录
{% raw %}
	git rm -rf dir 

	git clean -fd 
{% endraw %}
 