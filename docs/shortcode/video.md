---
title: video
date: 2021-03-14 00:14:13
permalink: /pages/4d3c13/
categories:
  - docs
  - shortcode
tags:
  - 
---
# 视频

Argon 提供了一些短代码的支持。

在文章中插入短代码即可让其被解析。

## 介绍

该短代码可以插入一个视频。

## 用法

```
[video 参数名="参数值"][/video]
```

>内容是必需的

## 参数

| 参数名   | 可选值     | 默认值 | 解释         | 是否必须 |
| -------- | ---------- | ------ | ------------ | -------- |
| url      | 字符串     | 无     | 视频地址     | 是       |
| width    | 整数       | auto   | 视频宽度     | 否       |
| height   | 整数       | auto   | 视频高度     | 否       |
| autoplay | true/false | false  | 是否自动播放 | 否       |

>参数不是必需的，如果不写某个参数则会使用默认值

## 例子

### 代码

```
[video url="https://xxxxx.com/xxxxx.mp4"][/video]
[video url="https://xxxxx.com/xxxxx.mp4" height="240" width="320"][/video]
[video url="https://xxxxx.com/xxxxx.mp4" autoplay="true"][/video]
```

