---
layout: post
title: Jave 多种判断key是否在map中存在的方法
date: 2017-06-12
tags: Jave 
---

目录

* TOC 
{:toc}


## 第一种判断

```
HashMap map = new HashMap();  
map.put("1", "value1");  
map.put("2", "value2");  
  
Iterator keys = map.keySet().iterator();  
while(keys.hasNext()){  
    String key = (String)keys.next();  
    if("2".equals(key)){  
        System.out.println("存在key");  
    }  
}  
```

## 第二种判断

```
boolean flag=map.containsKey("opt") 
```

