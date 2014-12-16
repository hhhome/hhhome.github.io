---
layout: post
title: Post with a Background Image
description: "Sample post with a background image CSS override."
tags: [sample post]
image:
  background: triangular.png
---

jekyll是一个类似于WordPress简单的免费的Blog生成工具。与WordPress不同的是: jekyll是一个生成静态网页的工具，不需要数据库支持

{% highlight yaml %}
image:
  background: filename.png
{% endhighlight %}

<!--more-->

This little bit of YAML makes the assumption that your background image asset is in the `/images` folder. If you place it somewhere else or are hotlinking from the web, just include the full http(s):// URL. Either way you should have a background image that is tiled.

If you want to set a background image for the entire site just add `background: filename.png` to your `_config.yml` and BOOM --- background images on every page!

<div xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/" about="http://subtlepatterns.com" class="notice">Background images from <span property="dct:title">Subtle Patterns</span> (<a rel="cc:attributionURL" property="cc:attributionName" href="http://subtlepatterns.com">Subtle Patterns</a>) / <a rel="license" href="http://creativecommons.org/licenses/by-sa/3.0/">CC BY-SA 3.0</a></div>