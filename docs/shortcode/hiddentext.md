---
title: hiddentext
date: 2021-03-14 00:14:13
permalink: /pages/d8ca96/
categories:
  - docs
  - shortcode
tags:
  - 
---
# 隐藏文本

Argon 提供了一些短代码的支持。

在文章中插入短代码即可让其被解析。

## 介绍

该短代码可以插入一段隐藏文本。

隐藏文本是一段无法直接看到的文本（模糊或者黑条），当鼠标移上后才会可见。

## 用法

```
[hidden 参数名="参数值"]内容[/hidden]
```

## 参数

| 参数名 | 可选值          | 默认值 | 解释                       | 是否必须 |
| ------ | --------------- | ------ | -------------------------- | -------- |
| type   | blur/background | blur   | 隐藏的形式 (模糊/黑条)     | 否       |
| color  | 字符串          | 无     | 鼠标移上一段时间后显示的话 | 否       |

>参数不是必需的，如果不写某个参数则会使用默认值

## 例子

### 代码

```
[hidden]一段隐藏的文本[/hidden]
[hidden type="background"]黑条隐藏文本[/hidden]
[hidden type="blur"]模糊隐藏文本[/hidden]
[hidden tip="你知道的太多了"]鼠标停留会有提示[/hidden]
```

### 效果

![](/_media/shortcode-hiddentext-example.png)

