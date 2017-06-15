---
layout: post
title: Jave JSON转换为XML
date: 2017-06-12
tags: Jave 
---

目录

* TOC 
{:toc}

## 方法

### JSON转换为XML

```
    /**  
     * json string convert to xml string 
     */    
    public static String json2xml(String jsonString){    
        XMLSerializer xmlSerializer = new XMLSerializer();    
        xmlSerializer.setTypeHintsEnabled(false);//是否保留元素类型标识，默认true  
        xmlSerializer.setElementName("e");//设置元素标签，默认e  
        xmlSerializer.setArrayName("a");//设置数组标签，默认a  
        xmlSerializer.setObjectName("o");//设置对象标签，默认o  
        return xmlSerializer.write(net.sf.json.JSONSerializer.toJSON(jsonString));    
    }  
```

### XML转换为JSON

```
 	/**  
     * xml string convert to json string 
     */    
    public static String xml2json(String xmlString){    
        XMLSerializer xmlSerializer = new XMLSerializer();    
        JSON json = xmlSerializer.read(xmlString);    
        return json.toString();    
    }    
```
[详细链接](http://blog.csdn.net/yuxiang19876021/article/details/51851340)
