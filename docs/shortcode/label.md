---
title: label
date: 2021-03-14 00:14:13
permalink: /pages/3f3b6b/
categories:
  - docs
  - shortcode
tags:
  - 
---
# 标签

Argon 提供了一些短代码的支持。

在文章中插入短代码即可让其被解析。

## 介绍

该短代码可以插入一个标签。

## 用法

```
[label 参数名="参数值"]内容[/label]
```

> 标签是行内元素，可在行内插入，不会独占一行

## 参数

| 参数名 | 可选值                       | 默认值 | 解释                  | 是否必须 |
| ------ | ---------------------------- | ------ | --------------------- | -------- |
| color  | indigo/green/red/blue/orange | indigo | 标签颜色              | 否       |
| shape  | square/round                 | square | 标签形状（方形/圆形） | 否       |

>有些参数不是必需的，如果不写某个参数则会使用默认值

## 例子

### 代码

```
方形
[label]默认标签[/label]
[label color="indigo"]靛蓝标签[/label]
[label color="green"]绿色标签[/label]
[label color="red"]红色标签[/label]
[label color="blue"]蓝色标签[/label]
[label color="orange"]橙色标签[/label]
圆形
[label color="indigo" shape="round"]靛蓝标签[/label]
[label color="green" shape="round"]绿色标签[/label]
[label color="red" shape="round"]红色标签[/label]
[label color="blue" shape="round"]蓝色标签[/label]
[label color="orange" shape="round"]橙色标签[/label]
```

### 效果

![](/_media/shortcode-label-example.png)