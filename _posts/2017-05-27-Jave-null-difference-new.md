---
layout: post
title: Jave BookInfo bookinfo=null;与BookInfo bookinfo=new BookInfo();的区别
date: 2017-05-25
tags: Jave 
---

目录

* TOC 
{:toc}

## 分析

1.java里对象传递的时候，传递的都是**引用**（也就是对象的地址），这比传递整个对象高效的多。<br/>
而基础类型，int，double等传递的才是值。

2.比如(new ArrayList<String>).add(new String("hello"))，jvm只是把new String("hello")的地址存入到了列表list里面。<br/>String str = new String("Test")，是开辟内存放入了对象，并把它的引用赋给str。

3.BookInfo bookinfo=null与BookInfo bookinfo=new BookInfo()<br/>
&nbsp;&nbsp;前者，是声明了一个**对象的引用**，jvm并没有开辟内存放入一个对象.<br/>
&nbsp;&nbsp;而后者，在声明了一个对象的引用后，又把新开辟的没有存储任何有效值的对象的地址赋给了他。<br/>
&nbsp;&nbsp;bookinfo=test.getinfo()，又把它指向了另一个地址.<br/>
&nbsp;&nbsp;也就是说原来开辟的内存并没有用，那就没有意义。但是java虚拟机自动垃圾回收机制会判断并回收
&nbsp;&nbsp;内存的。。