# 微企点 Css规范 #
------------------------------
[TOC]
## 文件名
使用小写字母，复合词以 - 分隔; 例如 nav.css , login-nav.css , login-page
## CSS 格式
- 不允许使用行内样式和style
- 选择器单独占一行，每个属性占一行，避免用单行CSS格式。属性声明要有缩进。
- 选择器要尽可能短，并且尽量限制组成选择器的元素个数，建议不要超过 3 


- 建议： 关联或孩子样式要增加2-4个空格的缩进。这样有利于分层查看和组织，可读性更好。
- 给一个样式指定多个选择器时，把每个选择器单独放一行。
- 让规则越具体越好
  尽量不要使用 ul li a 这样长的选择符，最好使用  .list-anchor 之类的选择符。
- 避免使用后代选择符
  通常处理后代选择符开销最高，使用字选择符更高效，最好使用下一条代替。
- 避免使用标签子选择符
  如果有如： #header > li > a，这样基于子标签的自选择符，那么应该使用一个class来关联每个元素如： .header-anchor。尽量使用具体的类代替子选择符。

```css
.post-list li a{
	color:#A8A8A8;
}
	.post-list li a:hover{
		color:#000;
		text-decoration:none;
	}
	.post-list li .author a,
	.post-list li .author a:hover{
		color:#F30;
		text-transform:uppercase;
	}
```

###id 和类的命名
- 为 id 和样式类使用有意义或通用的名字，避免由于 css 命名更改引起的不必要的文档或模板改变；例如
```css
    /* 不推荐： 无意义 */
    #yee-1901 {}

    /* 不推荐： 表现层的命名 */
    .button-green {}
    /* 推荐: 具体 */
    #gallery {}
    #login {}
    .video {}

    /* 推荐: 通用 */
    .effect {}
    .alt {}
    id 和 class 的命名长度应该适中，不要太简略也不要太详细；例如

    /* 不推荐 */
    #navigation {}
    .atr {}
    /* 推荐 */
    #nav {}
    .author {}
```

