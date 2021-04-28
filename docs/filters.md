# Filters

[Filter](https://developer.wordpress.org/plugins/hooks/filters/) 是 Wordpress 提供的特性，允许使用插件/子主题来对主题中一些值进行过滤。

欲添加一个 Filter，可以使用 `add_filter` 函数，该函数接受两个参数，第一个为 filter 的名称，第二个为过滤函数。Wordpress 将待过滤的内容传参传入过滤函数，过滤函数返回过滤后的结果。详见 [Wordpress 文档](https://developer.wordpress.org/plugins/hooks/filters/)。


Argon 主题提供以下 Filters。

---

| 名称      | 含义 |
| ----------- | ------ |
| argon_post_thumbnail   | 文章头图 URL |
| argon_comment_ua_icon   | 评论区 UA 图标 HTML |
| argon_comment_mail_notification_content   | 评论被回复时通知邮件的 HTML 内容 |
| argon_emotion_list   | 评论表情数组，详见 [评论表情](/emotions) 章节 |
| argon_darkmode_time_check   | 夜间模式切换为 "根据时间切换" 时的 Javascript 判断表达式|


欢迎通过 Issue / PR 来增加有必要的 Filter。
