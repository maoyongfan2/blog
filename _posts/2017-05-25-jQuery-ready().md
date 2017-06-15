---
layout: post
title: jQuery 事件 - ready() 方法
date: 2017-05-25
tags: jQuery 
---

目录

* TOC 
{:toc}


## 实例

在文档加载后激活函数：

```
$(document).ready(function(){
  $(".btn1").click(function(){
    $("p").slideToggle();
  });
});
```
## 定义和用法

当 DOM（文档对象模型） 已经加载，并且页面（包括图像）已经完全呈现时，会发生 ready 事件。

由于该事件在文档就绪后发生，因此把所有其他的 jQuery 事件和函数置于该事件中是非常好的做法。正如上面的例子中那样。

ready() 函数规定当 ready 事件发生时执行的代码。

ready() 函数仅能用于当前文档，因此无需选择器。

允许使用以下三种语法：

### 语法 1 

	$(document).ready(function)

### 语法 2

	$().ready(function)

### 语法 3

	$(function)

| 参数        | 描述   |  
| --------   | -----  | 
| function    | 	必需。规定当文档加载后要运行的函数。 | 
	
### 提示和注释

提示：ready() 函数不应与 <body onload=""> 一起使用。