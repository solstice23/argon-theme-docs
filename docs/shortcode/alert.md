# 提示

Argon 提供了一些短代码的支持。

在文章中插入短代码即可让其被解析。

## 介绍

该短代码可以插入一个提示条。

## 用法

```
[alert 参数名="参数值"]内容[/alert]
```

>内容不是必写的，如果不写则只显示标题(如果有标题)

## 参数

| 参数名 | 可选值                                                       | 默认值 | 解释         | 是否必须 |
| ------ | ------------------------------------------------------------ | ------ | ------------ | -------- |
| title  | 字符串                                                       | 无     | 提示的标题   | 否       |
| color  | indigo/green/red/blue/orange                                 | indigo | 进度条颜色   | 否       |
| icon   | [Font Awesome](https://fontawesome.com/v4.7.0/icons/) 中的图标名称 (不带 fa-) | 无     | 标题前的图标 | 否       |

>参数不是必需的，如果不写某个参数则会使用默认值

## 例子

### 代码

```
[alert]默认提示[/alert]
[alert color="indigo"]靛蓝提示[/alert]
[alert color="green"]绿色提示[/alert]
[alert color="red"]红色提示[/alert]
[alert color="blue"]蓝色提示[/alert]
[alert color="orange"]橙色提示[/alert]
[alert color="black"]黑色提示[/alert]
[alert title="我是标题" color="indigo"]带标题的提示[/alert]
[alert icon="flag" color="indigo"]带图标的提示[/alert]
[alert title="我是标题" icon="flag" color="indigo"]带标题和图标的提示[/alert]
```

### 效果

![](/_media/shortcode-alert-example.png)

