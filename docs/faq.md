# FAQ

常见问题解答

## Q: 检测不到更新/检测到了但更新失败

A: 在 Argon 设置中切换更新源，国外主机选择 Github，国内的主机一般选择 jsdelivr。

## Q: 依旧更新失败或页面顶部出现 Warning？

A: 检查 `/wp-content/themes` 下的主题目录名称是否为 `argon`。

## Q: 安装了某个插件，初次进入某个页面可以工作，但是从别的页面跳转进入工作不正常

A: 请将该插件的初始化代码写入 Pjax 回调中或关闭 Pjax。Argon 设置页中有 Pjax 回调的说明。

## Q: 错误 `Parse error: syntax error, unexpected '?' in xxx`

A: 请升级 PHP 版本至 7.0 及以上。

## Q: 评论失败

A: 请检查 Wordpress 是否安装在子目录，如果是，请在 Argon 设置中设置子目录的路径。

如果仍旧评论失败，请检查是否是相关插件导致。

如果仍旧评论失败，请查看 Chrome Developer Tool 中 Network 菜单的 `admin-ajax.php` 请求，发 Issue 或在评论区反馈。

## Q: 安装了 Editor.md 插件，Console 报错

A: 请打开 Editor.md 插件的兼容模式。

## Q: 邮件无法发送/开启了评论邮件提醒却收不到邮件

A: 需要安装邮件相关的插件，例如 `WP Mail SMTP`。

## Q: 说说页面/邮件退订页面 404

A: 可能是 Wordpress 伪静态缓存未及时更新。请到 "Wordpress 管理后台-设置-固定链接" 页面中直接点击 "保存更改" 来刷新缓存。

如果使用的是 Nginx，可能需要添加伪静态：

```
rewrite /unsubscribe-comment-mailnotice/?(.*)$ /wp-content/themes/argon/unsubscribe-comment-mailnotice.php$1;
```

## Q: 我编辑了主题的文件，但是主题更新后编辑的内容消失了

A: 如果你希望修改主题，不建议直接修改主题文件，更新主题时会被替换。

如果你想增加新的 CSS，可以在 `Wordpress 后台 - 外观 - 自定义 - 额外CSS` 中添加。

如果你想添加 JS，可以在 `Argon 设置 - 页头/页尾脚本` 中添加。

如果你想在 function.php 中添加新的方法，或者修改主题的某几个文件，推荐使用[子主题](https://codex.wordpress.org/zh-cn:子主题)方式。

## Q: 有部分链接没有 HTTPS，浏览器显示 "与此网站建立的链接并非完全安全"

A: 请检查 "Wordpress 设置 - 常规" 中的 "WordPress地址（URL）" 和 "站点地址（URL）" 两项是否为 HTTPS。

## Q: 是否会移植到 XXX 博客框架

A: 没有计划也没有精力移植，不过欢迎 Fork 子项目移植到不同框架

## Q: 有 BUG/我想要新功能

A: 欢迎通过以下方式向我反馈

- [Github Issue](https://github.com/solstice23/argon-theme/issues/new)
- 在[主题博客](https://solstice23.top/archives/746)的评论区发送评论
- Telegram [@solstice233](https://t.me/solstice233)
