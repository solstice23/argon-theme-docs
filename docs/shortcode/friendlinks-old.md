# 友情链接列表 (旧)

Argon 提供了一些短代码的支持。

在文章中插入短代码即可让其被解析。

## 介绍

该短代码可以插入一个友情链接模块。

> 不推荐使用此短代码。
>
> 自 Argon V0.902 版本开始，友情链接使用 Wordpress 自带的链接管理器来管理。请使用新的友情链接列表短代码来插入友情链接模块。
>
> 为保留旧特性，此短代码不会被移除，但不推荐使用。

!> 自 Argon V0.902 版本开始，此短代码更名为 `sfriendlinks`

## 用法

```
[sfriendlinks]
category|分组标题
link|地址|名称|描述|头像
[/sfriendlinks]
```

每行中用竖线分隔。

第一项为 `link`，则该行为链接；如果为 `category`，那么该行为分组标题。

对于每种情况，上方代码给出了解释，你也可以参考底部的例子。

> 可以没有 `category` 行，此时链接不会分组

> 描述和头像可省略

## 参数

| 参数名  | 可选值     | 默认值 | 解释             | 是否必须 |
| ------- | ---------- | ------ | ---------------- | -------- |
| shuffle | true/false | false  | 随机顺序输出友链 | 否       |

>参数不是必需的，如果不写某个参数则会使用默认值

## 例子

### 代码

```
[sfriendlinks]
category|分组1
link|https://google.com|Google|谷歌|https://xxxx.xxx/xxx.png
link|https://github.com|Github
link|http://codeforces.com|Github|CF
category|分组2
link|https://bilibili.com|Bilibili|哔哩哔哩|
link|https://zhihu.com|知乎|分享你刚编的故事|
[/sfriendlinks]
```

### 效果

![](/_media/shortcode-frindlinks-example.png)

