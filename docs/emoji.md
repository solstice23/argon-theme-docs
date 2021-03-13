# 评论表情

想要自定义评论表情，请参见以下步骤。

---

## Filter

使用 `argon_emotion_list` filter 来应用自定义的评论表情列表。

```
add_filter('argon_emotion_list' , 'callback_function');
```

回调函数将被传入一个参数，即表情列表数组。回调函数应该修改这个数组为想要的新表情列表，并返回修改后的数组。

## 结构

```
┌-EmotionArray
├-┬-Group
│ ├--groupname
│ ├--description
│ └-┬list
│   ├-┬Emotion
│   │ ├-type: text
│   │ ├-text
│   │ └-title
│   ├-┬Emotion
│   │ ├-type: sticker
│   │ ├-src
│   │ ├-code
│   │ └-title
│   ├-Emotion
│   └-Emotion
├---Group
└---Group
```

## 表情数组

表情数组(EmotionArray)的每一项也是一个数组，表示一个表情组(Group)。

## 表情组

表情组是一个关联数组，每一项的含义如下。

| 数组项      | 类型   | 含义                                                   | 是否必须 |
| ----------- | ------ | ------------------------------------------------------ | -------- |
| groupname   | 字符串 | 该表情组的名称                                         | 必须     |
| description | 字符串 | 该表情组的介绍，如存在会显示在该表情组的表情列表的下方 | 可选     |
| list        | 数组   | 包含该表情组所有的表情(Emotion)                        | 必须     |

## 表情

表情是一个关联数组，其中的 type 项表示该表情的类型，有两种（字符表情和图片表情），每种表情的格式不同。每一项的含义如下。

### 1.字符表情 (text)

| 数组项 | 类型   | 含义                                           | 是否必须 |
| ------ | ------ | ---------------------------------------------- | -------- |
| type   | 字符串 | 值为 text，表示该表情是一个字符表情            | 是       |
| text   | 字符串 | 该字符表情的字符串，例如一个颜文字             | 是       |
| title  | 字符串 | 该表情的名称，鼠标放在该表情上一段时间后会显示 | 否       |

### 2.图片表情 (sticker)

| 数组项 | 类型   | 含义                                                         | 是否必须 |
| ------ | ------ | ------------------------------------------------------------ | -------- |
| type   | 字符串 | 值为 sticker，表示该表情是一个图片表情                       | 是       |
| src    | 字符串 | 该表情图片的地址                                             | 是       |
| code   | 字符串 | 该表情的代码，例如这里的值为 `xxx`，则评论里所有的 `:xxx:` 会被替换为该表情。不带冒号 | 是       |
| title  | 字符串 | 该表情的名称，鼠标放在该表情上一段时间后会显示               | 否       |

## 例子

一个表情数组的例子:

```
array(
		array(
			'groupname' => '颜文字', 
			'list' => array(
				array('type' => 'text', 'text' => "|´・ω・)ノ"),
				array('type' => 'text', 'text' => "ヾ(≧∇≦*)ゝ"),
				array('type' => 'text', 'text' => "(☆ω☆)")
			)
		),
		array(
			'groupname' => 'Emoji', 
			'list' => array(
				array('type' => 'text', 'text' => "😂"),
				array('type' => 'text', 'text' => "😀"),
				array('type' => 'text', 'text' => "😅")
			)
		),
		array(
			'groupname' => '小恐龙', 
			'list' => array(
				array('type' => 'sticker', 'code' => 'dinosaur-shy', 'src' => $GLOBALS['assets_path'] . '/stickers/dinosaur/1.jpg'),
				array('type' => 'sticker', 'code' => 'dinosaur-daze', 'src' => $GLOBALS['assets_path'] . '/stickers/dinosaur/2.jpg'),
				array('type' => 'sticker', 'code' => 'dinosaur-sweat', 'src' => $GLOBALS['assets_path'] . '/stickers/dinosaur/3.jpg'),
			)
		),
		array(
			'groupname' => '花!', 
			'list' => array(
				array('type' => 'sticker', 'code' => 'flower-flower', 'src' => $GLOBALS['assets_path'] . '/stickers/flower/1.jpg'),
				array('type' => 'sticker', 'code' => 'flower-grass', 'src' => $GLOBALS['assets_path'] . '/stickers/flower/2.jpg'),
				array('type' => 'sticker', 'code' => 'flower-leaf', 'src' => $GLOBALS['assets_path'] . '/stickers/flower/3.jpg'),
			),
			'description' => 'Source: github.com/k4yt3x/flowerhd'
		)
	);
```

一个插件的例子，该插件会往表情列表追加一套新的表情:

```php
<?php
/*
Plugin Name: Test
Description: This plugin will add a new emotion group
Version: 1.0
*/
	function add_more_emotions($emotionList){
		array_push(
			$emotionList,
			array(
				'groupname' => '要增加的表情包名', 
				'list' => array(
					array('type' => 'sticker', 'code' => 'test-1', 'src' => $GLOBALS['assets_path'] . '/stickers/test/1.jpg'),
					array('type' => 'sticker', 'code' => 'test-2', 'src' => $GLOBALS['assets_path'] . '/stickers/test/2.jpg'),
					array('type' => 'sticker', 'code' => 'test-3', 'src' => $GLOBALS['assets_path'] . '/stickers/test/3.jpg')
				)
			)
		);
		return $emotionList;
	}
	add_filter('argon_emotion_list' , 'add_more_emotions');
?>
```