# 贡献指南

欢迎以 Pull Request 的形式对 Argon 作出贡献。下面是贡献指南和一些需要注意的地方。

## 代码风格

### 变量命名

名字不要太随意即可 <spoiler>(例如 OI 中的命名很大一部分是不被接受的)</spoiler>

PHP 函数名、HTMl ID 名: 下划线命名

PHP 变量名、JS 变量名、CSS 类名: 驼峰命名

### 缩进

使用 Tab 缩进

## 测试

新功能需要不影响以前的 UI，不会使 UI 出现显示问题（例如在工具栏增加了一个图标，但是工具栏高度变化了），除非本身是针对 UI 的改进。

新功能的 UI 应该与主题统一。

新功能对于不同的情况，应该不出现错误。

## 本地化指南

### PHP

因为 Argon 中字符串的语言是中文，所以对语言做了归一处理，对尚未本地化的语言，默认使用英文翻译。

要增加一种语言，请在 `function.php` 中的 `argon_locate_filter` 函数中增加相应语言的处理逻辑。

翻译文件位于 `languages` 目录中，使用 Poedit (或其他 .po 编辑软件) 进行编辑并编译。

从代码中提取待翻译字符串时需要排除的路径:
```
assets\
languages\
theme-update-checker\
gutenberg\
argontheme.js
```

### Javascript

翻译字符串位于 `argontheme.js` 的 `translation` 数组中，在该数组中增加相应语言的翻译即可。

### Gutenberg 编辑器

翻译字符串位于 `gutenberg/src/i18n` 目录中，新建相应语言的翻译 `.js` 文件，再在 `i18n.js` 中引入 `translation` 数组，构建即可。

## 完善文档

### 格式

使用 Markdown 格式编写文档。新建相应的 `.md` 文件，并在 `_sidebar.md` 中添加该文件即可。

第一行使用一个一级标题，写出该页面的名称，文档会自动将其设为页面的大标题。其余标题使用二级及以下。