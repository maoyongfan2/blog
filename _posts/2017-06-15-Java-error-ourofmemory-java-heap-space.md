---
layout: post
title: Jave 报错总结之OutOfMemoryError:Java heap space
date: 2017-06-15
tags: JaveError 
---

目录

* TOC 
{:toc}

## 哪些情况可以触发该报错

1. 程序进入死循环 
2. JAVA的堆栈设置太小的原因 

## 解决JAVA的堆栈设置太小的方法

1. 可以在windows 更改系统环境变量
加上JAVA_OPTS=-Xms64m -Xmx512m

2. set JAVA_OPTS= -Xms32m -Xmx1024m
