---
title: collapse
date: 2021-03-14 00:14:13
permalink: /pages/2c8f2a/
categories:
  - docs
  - shortcode
tags:
  - 
---
# 折叠区块

Argon 提供了一些短代码的支持。

在文章中插入短代码即可让其被解析。

## 介绍

该短代码可以插入一个折叠区块，点击该折叠区块可以展开或收缩。

## 用法

```
[collapse 参数名="参数值"]内容[/collapse]
```

>内容是必需的

## 参数

| 参数名    | 可选值                                                       | 默认值 | 解释         | 是否必须 |
| --------- | ------------------------------------------------------------ | ------ | ------------ | -------- |
| title     | 字符串                                                       | 无     | 折叠区块标题 | 是       |
| color     | indigo/green/red/blue/orange                                 | indigo | 提示的颜色   | 否       |
| icon      | [Font Awesome](https://fontawesome.com/v4.7.0/icons/) 中的图标名称 (不带 fa-) | 无     | 标题前的图标 | 否       |
| collapsed | true/false                                                   | true   | 默认是否折叠 | 否       |

>一些参数不是必需的，如果不写某个参数则会使用默认值例子

### 代码

```
[collapse title="默认折叠区块"]折叠的内容[/collapse]
[collapse title="靛蓝折叠区块" color="indigo"]折叠的内容[/collapse]
[collapse title="绿色折叠区块" color="green"]折叠的内容[/collapse]
[collapse title="红色折叠区块" color="red"]折叠的内容[/collapse]
[collapse title="蓝色折叠区块" color="blue"]折叠的内容[/collapse]
[collapse title="橙色折叠区块" color="orange"]折叠的内容[/collapse]
[collapse title="黑色折叠区块" color="black"]折叠的内容[/collapse]
[collapse title="灰色折叠区块" color="grey"]折叠的内容[/collapse]
[collapse title="无色折叠区块" color="none"]折叠的内容[/collapse]
[collapse title="显示左边框的折叠区块" showleftborder="true"]折叠的内容[/collapse]
[collapse title="带图标的折叠区块" icon="flag"]折叠的内容[/collapse]
[collapse title="默认展开的折叠区块" collapsed="false"]折叠的内容[/collapse]
```

### 效果

![](/_media/shortcode-collapse-example.png)

