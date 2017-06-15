---
layout: post
title: Jave replaceAll() 方法
date: 2017-06-14
tags: Jave 
---

目录

* TOC 
{:toc}


## replaceAll() 方法

### 语法
```
public String replaceAll(String regex,
                         String replacement)
```

### 参数
* **regex** -- 匹配此字符串的正则表达式。
* **newChar** -- 用来替换每个匹配项的字符串。

### 返回值
成功则返回替换的字符串，失败则返回原始字符串。

### 实例
```
public class Test {
	public static void main(String args[]) {
		String Str = new String("www.google.com");

		System.out.print("匹配成功返回值 :" );
		System.out.println(Str.replaceAll("(.*)google(.*)",
                            "runoob" ));
		System.out.print("匹配失败返回值 :" );
		System.out.println(Str.replaceAll("(.*)taobao(.*)",
                            "runoob" ));
	}
}
```
**输出:**<br/>
以上程序执行结果为：<br/>
匹配成功返回值 :runoob<br/>
匹配失败返回值 :www.google.com