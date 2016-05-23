---
layout:post
title: git config
description: "git 配置"
tags: [sample post]
image:
  feature: abstract-5.jpg
---

# git config

 通过 git config 可以设置Git 外观和行为的配置变量, 这些变量存储在三个不同的位置：

 * /etc/gitconfig 文件: 包含系统上每一个用户及他们仓库的通用配置。 如果使用带有 --system 选项的 git config 时，它会从此文件读写配置变量。
 * ~/.gitconfig 或 ~/.config/git/config 文件：只针对当前用户。 可以传递 --global 选项让 Git 读写此文件。
 * 当前使用仓库的 Git 目录中的 config 文件（就是 .git/config）：针对该仓库。

 每一个级别覆盖上一级别的配置，所以 .git/config 的配置变量会覆盖 /etc/gitconfig 中的配置变量。

在 Windows 系统中，Git 会查找 $HOME 目录下（一般情况下是 C:\Users\$USER）的 .gitconfig 文件。 Git 同样也会寻找 /etc/gitconfig 文件，但只限于 MSys 的根目录下，即安装 Git 时所选的目标位置


#### 设置全局用户名和邮箱

{% highlight bash %}

$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com

{% endhighlight %}


#### 检查配置信息

{% highlight bash %}

$ git config --list

{% endhighlight %}


{% highlight bash %}

git config <key>： 来检查 Git 的某一项配置

git config user.name

{% endhighlight%}
