# 让短代码不被解析

如果你不想让某段内容中的短代码被解析，想原样输出这段内容，只需要将这段内容用 `[noshortcode][/noshortcode]` 包裹即可。

## 用法

```
[noshortcode]内容[/noshortcode]
```

## 例子

### 代码

```
[noshortcode]
这段内容中的短代码将不会被解析
[alert]我不会被解析[/alert]
[/noshortcode]
```

### 效果

> 这段内容中的短代码将不会被解析
>
> [alert]我不会被解析[/alert]