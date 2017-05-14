# 微企点 文章管理平台 Css规范 #
------------------------------
<!-- [TOC] -->

## 基本命名
- 所有class或id的命名全部使用小写字母，复合词以 - 分隔；**禁止使用**例如： ~~“.loginNav”~~，~~“.loginPage”~~，~~“#contentPage”~~ 等驼峰命名方式进行命名。

- 对于放到component层，或者单独独立出来的一个模块，最外层class或者id的命名，一定要以“wqd-”开头。例如： “.wqd-tips-mask”，“.wqd-tips”，“.wqd-list”等。

- **注意**：在以“wqd-”开头方式命名时，使用时一定要先进行一次全文检索，防止重名。

## 书写规范
1. Css代码书写时，选择器的第一个元素一定是以“wqd-”开头方式命名的。
2. Css代码书写时，选择器的第一个元素一定是这一部分模块的最外层class或者id。
3. Css代码书写时，对于每一个模块的书写，统一都要增加注释，注释方式统一为：“/* */”这种方式。
```
/* good css below */
    /* tips css start */
    .wqd-tips .tips-hd {...}
    .wqd-tips .tips-hd .hd-title {...}
    .wqd-tips .tips-hd .hd-more {...}
        /* tips warn */
    .wqd-tips.warning {...}
        /* tips del */
    .wqd-tips.del {...}
    ......
    /* tips css end */
    
/* bad css below */
    .wqd-tips .tips-hd {...}
    .wqd-tips .tips-hd .hd-title {...}
    .wqd-tips .tips-hd .hd-more {...}
    .wqd-tips.warning {...}
    .wqd-tips.del {...}
    ......

    // tips css
    .wqd-tips .tips-hd {...}
    .wqd-tips .tips-hd .hd-title {...}
    .wqd-tips .tips-hd .hd-more {...}
    // tips warn
    .wqd-tips.warning {...}
    .wqd-tips.del {...}
    ......
```
4. Css代码书写时，选择器中组成的元素个数，尽量不要超过3个。
```
/* good css below */
    .wqd-list .list-hd {...}
    .wqd-list .list-hd .hd-title {...}
    .wqd-list .list-hd .hd-more {...}

/* bad css below */
    .wqd-list .list-hd .list-content .hd-title {...}
    .wqd-list .list-hd .list-content .list-btn .hd-title {...}
```
5. Css代码书写时，样式书写顺序和事例如下：
    1. 位置属性(display, float, position, top, bottom, left, right, z-index等)
    2. 大小(width, height, padding, margin)
    3. 文字系列(font, line-height, color, text-align, letter-spacing等)
    4. 背景(background, border等)
    5. 其他(animation, transition等) 
```
/* good css below */
    .wqd-tips {position:fixd;top:0;z-index:1001;color:#fff;;background-color:#fff;border-radius:3px;}

/* bad css below */
    .wqd-tips {border-radius:3px;top:0;position:fixd;z-index:1001;color:#fff;;background-color:#fff;}
    .wqd-tips {z-index:1001;top:0;position:fixd;border-radius:3px;color:#fff;;background-color:#fff;}
```
6. Css代码书写时，样式内容跟选择器之间一定要存在空格，属性值设置时，之间一定不能有空格。
```
/* good css below */
    .wqd-tips {width:100px;}

/* bad css below */
    .wqd-tips{width:100px;}
    .wqd-tips {width: 100px;}
    .wqd-tips { width:100px; }
```




