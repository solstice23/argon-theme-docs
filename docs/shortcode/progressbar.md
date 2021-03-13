---
title: progressbar
date: 2021-03-14 00:14:13
permalink: /pages/3d630e/
categories:
  - docs
  - shortcode
tags:
  - 
---
# 进度条

Argon 提供了一些短代码的支持。

在文章中插入短代码即可让其被解析。

## 介绍

该短代码可以插入一个进度条。

## 用法

```
[progressbar 参数名="参数值"]进度条标签内容[/progressbar]
```

>进度条标签内容可以不填写，不填写会隐藏进度条标签

## 参数

| 参数名   | 可选值                       | 默认值 | 解释       | 是否必须 |
| -------- | ---------------------------- | ------ | ---------- | -------- |
| progress | 0 ~ 100的数字                | 100    | 进度百分比 | 否       |
| color    | indigo/green/red/blue/orange | indigo | 进度条颜色 | 否       |

>参数不是必需的，如果不写某个参数则会使用默认值

## 例子

### 代码

```
[progressbar progress="20"]默认进度条[/progressbar]
[progressbar progress="30" color="indigo"]靛蓝进度条[/progressbar]
[progressbar progress="40" color="green"]绿色进度条[/progressbar]
[progressbar progress="66" color="red"]红色进度条[/progressbar]
[progressbar progress="80" color="blue"]蓝色进度条[/progressbar]
[progressbar progress="100" color="orange"]橙色进度条[/progressbar] 
[progressbar progress="23"][/progressbar]
[progressbar]没有指明参数的进度条[/progressbar]
[progressbar progress="66.66"]小数进度条[/progressbar]
```

### 效果

![](/_media/shortcode-progressbar-example.png)

