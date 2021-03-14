# Github 信息卡

Argon 提供了一些短代码的支持。

在文章中插入短代码即可让其被解析。

## 介绍

该短代码可以插入一个 Github Repo 信息卡，可以跳转到相应的 Github Repo 地址，显示介绍、Star数、Fork 数预览。

## 用法

```
[github 参数名="参数值"][/github]
```

## 参数

| 参数名  | 可选值           | 默认值   | 解释                           | 是否必须 |
| ------- | ---------------- | -------- | ------------------------------ | -------- |
| author  | 字符串           | 空       | 欲展示的 Repo 的作者用户名     | 是       |
| color   | 字符串           | 空       | 欲展示的 Repo 名               | 是       |
| size    | full/mini        | full     | 尺寸                           | 否       |
| getdata | frontend/backend | frontend | 前端/后端获取 Github Repo 信息 | 否       |

## 例子

### 代码

```
 [github author="solstice23" project="argon-theme"][/github]
```

### 效果

![](/_media/shortcode-github-example.png)

