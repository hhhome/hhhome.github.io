---
layout: post
title: javascript 冒泡事件
description: "javascript dom 冒泡捕获事件"
tags: [sample post]
image:
  feature: abstract-5.jpg
---


DOM事件机制包含冒泡和捕获两种，按照topmost element->innermost element方向传递事件被称为捕获方式，而从innermost element->topmost element方向传递事件被称为冒泡方式。

### 事件委托

就是把事件处理器（或监听器）添加到parent元素上，避免把其添加到多个子元素上。

### 让不同对象捕获同一事件

这个其实是给不同对象绑定相同的触发事件，比如点击onclick,当点击其中一个的话，所有这些对象就会触发各自所对应的函数操作。

<!--more -->

### 阻止事件冒泡

先要清楚什么时候需要阻止事件冒泡：比如document上有A事件，div有B事件，div里的span有C事件（ABC是同类型事件，比如都是onclick），若不给div和span阻止事件冒泡的话，点击span时就会触发到B、C事件。所以事件冒泡可能会激活我们本来不想激活的事件，导致程序错乱，所以必要时，我们要阻止事件冒泡。

阻止冒泡事件要考虑浏览器的兼容问题：


{% highlight javascript %}

if(Event.stopPropagation){

  Event.stopPropagation();      //非IE

}else{

  Event.cancelBubble=true;    //IE

}

{%endhighlight%}
