# TODO 复选框

Argon 提供了一些短代码的支持。

在文章中插入短代码即可让其被解析。

## 介绍

该短代码可以插入一个复选框（不可互动）。

## 用法

```
[checkbox 参数名="参数值"]内容[/checkbox]
```

## 参数

| 参数名  | 可选值     | 默认值 | 解释           | 是否必须 |
| ------- | ---------- | ------ | -------------- | -------- |
| checked | true/false | false  | 是否勾选复选框 | 否       |
| inline  | true/false | false  | 是否行内显示   | 否       |

> 有些参数不是必需的，如果不写某个参数则会使用默认值

## 例子

### 代码

```
[checkbox]默认复选框[/checkbox]
[checkbox checked="true"]已经完成的项目[/checkbox]
[checkbox checked="false"]还未完成的项目[/checkbox]
```

### 效果

![](/_media/shortcode-checkbox-example.png)