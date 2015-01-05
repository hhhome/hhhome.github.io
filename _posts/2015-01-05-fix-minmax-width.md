---
layout: post
title: minmax-width-height
description: "兼容ie6的最小宽度，最大高度，最大宽度，最小高度 css 写法"
tags: [sample post]
image:
  feature: abstract-8.jpg
---

最小宽度，最大高度



{% highlight css %}
 .wrap{min-width:920px;_width:expression((document.documentElement.clientWidth||document.body.clientWidth)<920?"920px":""); background: #ff0;max-height:270px;
_height:expression(this.scrollHeight > 270 ? "270px" : "auto"); overflow-y:auto; }
{% endhighlight %}

<!--more-->

最大宽度，最小高度

{% highlight css %}
.wrap2{max-width:920px;_width:expression((document.documentElement.clientWidth||document.body.clientWidth)>920?"920px":""); background: #ff0; min-height:270px;
_height:expression(this.scrollHeight < 270 ? "270px" : "auto"); overflow-x:auto;  margin:0 auto;}

{% endhighlight %}


