---
title: admonition
date: 2021-03-14 00:14:13
permalink: /pages/dc4c5e/
categories:
  - docs
  - shortcode
tags:
  - 
---
# 警告

Argon 提供了一些短代码的支持。

在文章中插入短代码即可让其被解析。

## 介绍

该短代码可以插入一个警告。

## 用法

```
[admonition 参数名="参数值"]内容[/admonition]
```

>内容不是必写的，如果不写则只显示标题(如果有标题)

## 参数

| 参数名 | 可选值                                                       | 默认值 | 解释                      | 是否必须 |
| ------ | ------------------------------------------------------------ | ------ | ------------------------- | -------- |
| title  | 字符串                                                       | 无     | 警告的标题                | 否       |
| color  | indigo/green/red/blue/orange                                 | grey   | 警告的颜色                | 否       |
| icon   | [Font Awesome](https://fontawesome.com/v4.7.0/icons/) 中的图标名称 (不带 fa-) | 无     | 标题前的图标 (如果有标题) | 否       |

>参数不是必需的，如果不写某个参数则会使用默认值

## 例子

### 代码

```
[admonition]默认警告[/admonition]
[admonition title="我是标题" color="indigo"]靛蓝警告[/admonition]
[admonition title="我是标题" color="green"]绿色警告[/admonition]
[admonition title="我是标题" color="red"]红色警告[/admonition]
[admonition title="我是标题" color="blue"]蓝色警告[/admonition]
[admonition title="我是标题" color="orange"]橙色警告[/admonition]
[admonition title="我是标题" color="black"]黑色警告[/admonition]
[admonition title="我是标题" color="grey"]灰色警告[/admonition]
[admonition title="我是标题" icon="flag" color="indigo"]带标题和图标的警告[/admonition]
[admonition color="indigo"]不带标题的警告[/admonition]
[admonition title="只有标题的警告" color="indigo"][/admonition]
[admonition title="只有标题和图标的警告" icon="flag" color="indigo"][/admonition]
```

### 效果

![](/_media/shortcode-admonition-example.png)

