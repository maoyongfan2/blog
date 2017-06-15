---
layout: post
title: Jave 常用小方法
date: 2017-06-12
tags: Jave 
---

目录

* TOC 
{:toc}


## 方法介绍

### 转为小写

**toLowerCase();**

### list是否包含某个字符串 

```
	注意list为null时，用contains方法会引发空指针异常
	public static void main(String[] args){

	    List<String> list = new ArrayList<String>();

	    list.add("fei");
	    list.add("long");
	    list.add("feilong");

	    System.out.println(list.contains("feilong"));
	}
```

### 遍历map中的键值

```
Map<String, String> map = new HashMap<String, String>();
map.put("1", "value1");
map.put("2", "value2");
map.put("3", "value3");

//第一种：普遍使用，二次取值
System.out.println("通过Map.keySet遍历key和value：");
for (String key : map.keySet()) {
System.out.println("key= "+ key + " and value= " + map.get(key));
}

//第二种
System.out.println("通过Map.entrySet使用iterator遍历key和value：");
Iterator<Map.Entry<String, String>> it = map.entrySet().iterator();
while (it.hasNext()) {
Map.Entry<String, String> entry = it.next();
System.out.println("key= " + entry.getKey() + " and value= " + entry.getValue());
}

//第三种：推荐，尤其是容量大时
System.out.println("通过Map.entrySet遍历key和value");
for (Map.Entry<String, String> entry : map.entrySet()) {
System.out.println("key= " + entry.getKey() + " and value= " + entry.getValue());
}
//第四种
System.out.println("通过Map.values()遍历所有的value，但不能遍历key");
for (String v : map.values()) {
System.out.println("value= " + v);
}
}
```
### 获取Map大小

**map.size();**

### 判断字符串是否包含字符串

**string.indexOf(sub);**

