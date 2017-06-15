---
layout: post
title: jQuery 遍历 - each()方法
date: 2017-06-15
tags: jQuery
---

目录

* TOC 
{:toc}

## 定义和用法
each() 方法规定为每个匹配元素规定运行的函数。<br/>
提示：返回 false 可用于及早停止循环。

## 语法
	$(selector).each(function(index,element))

|  参数  | 描述   | 
| --------   | -----  |
|function(index,element)|必需。为每个匹配元素规定运行的函数.<br/> 1.index - 选择器的 index 位置<br/>2.element - 当前的元素（也可使用 "this" 选择器）|

## 实例
输出每个 li 元素的文本：
```
$("button").click(function(){
  $("li").each(function(){
    alert($(this).text())
  });
});
```