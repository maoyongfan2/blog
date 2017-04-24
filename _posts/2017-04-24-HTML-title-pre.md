---
layout: post
title: HTML-&lt;pre>
date: 2017-04-24
tags: HTML 
---

目录

* TOC 
{:toc}

## 介绍<pre>

### 定义

* pre 元素可定义预格式化的文本。被包围在 pre 元素中的文本通常会**保留空格和换行符**。而文本也会呈现为等宽字体。

* `<pre>` 标签的一个常见应用就是用来表示计算机的源代码。

* 可以导致段落断开的标签（例如标题、<p> 和 <address> 标签）绝不能包含在 <pre> 所定义的块里。尽管有些浏览器会把段落结束标签解释为简单地换行，但是这种行为在所有浏览器上并不都是一样的。


### 用法

* 样例

	<pre>
	&lt;html&gt;

	&lt;head&gt;
	  &lt;script type=&quot;text/javascript&quot; src=&quot;loadxmldoc.js&quot;&gt;
	&lt;/script&gt;
	&lt;/head&gt;

	&lt;body&gt;

	  &lt;script type=&quot;text/javascript&quot;&gt;
	    xmlDoc=<a href="dom_loadxmldoc.asp">loadXMLDoc</a>(&quot;books.xml&quot;);
	    document.write(&quot;xmlDoc is loaded, ready for use&quot;);
	  &lt;/script&gt;

	&lt;/body&gt;

	&lt;/html&gt;
	</pre>



效果：

<pre>
&lt;html&gt;

&lt;head&gt;
  &lt;script type=&quot;text/javascript&quot; src=&quot;loadxmldoc.js&quot;&gt;
&lt;/script&gt;
&lt;/head&gt;

&lt;body&gt;

  &lt;script type=&quot;text/javascript&quot;&gt;
    xmlDoc=<a href="dom_loadxmldoc.asp">loadXMLDoc</a>(&quot;books.xml&quot;);
    document.write(&quot;xmlDoc is loaded, ready for use&quot;);
  &lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;
</pre>



* 样例

		<!DOCTYPE html>
		<html>
		<head>
		<style>
		pre {
		    display: block;
		    font-family: monospace;
		    white-space: pre;
		    margin: 1em 0;
		} 
		</style>
		</head>
		<body>

		<p>A pre element is displayed like this:</p>

		<pre>
		is displayed in a fixed-width
		font, and it preserves
		both      spaces and
		line breaks
		</pre>

		<p>Change the default CSS settings to see the effect.</p>

		</body>
		</html>


