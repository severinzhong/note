# CSS NoteBook

## 基础语法

selector {declaration1; declaration2; ... declarationN }

其中 declaration 表示为: property: value

example :

```css
    h1{
        color : red; 
        background-color : rgb(255,0,0);
        font-size : 14px;
        text-align : center;
        font-family : arial;
        margin : 0% ;
        padding : 0 ;
    }
```    
在HTML中插入使用：
```html
    <link rel="stylesheet" type="text/css" href="mystyle.css" />

    <style type="text/css">
        hr {color: sienna;}
        p {margin-left: 20px;}
        body {background-image: url("images/back40.gif");}
    </style>
```


## selector

对于基本的HTML元素在css中的选择关联如下：

| HTML属性 | 选择器属性 |
|:--|:--|
|div...| div |
|class="name"|.name|
|id="name"|#name|

可以在一个selector中使用多个选择器用","隔开，而一个选择器可以使用多个基本元素表现继承关联等关系用空格表现。属性选择器对于属性能进行选择，规则如下：
| 属性 | 描述 |
|:--|:--|
|[attribute]	|用于选取带有指定属性的元素。
|[attribute=value]	|用于选取带有指定属性和值的元素。
|[attribute~=value]	|用于选取属性值中包含指定词汇的元素。
|[attribute\|=value]	|用于选取带有以指定值开头的属性值的元素，该值必须是整个单词。
|[attribute^=value]	|匹配属性值以指定值开头的每个元素。
|[attribute$=value]	|匹配属性值以指定值结尾的每个元素。
|[attribute*=value]	|匹配属性值中包含指定值的每个元素。
下面是一些例子：
```css
    *{
        margin: 0% ;
        margin-block-start: 0 ;
        margin-block-end: 0 ;
    }
    body strong {
        color : black ;
    }
    #sidebar p {
        font-style: italic;
        text-align: right;
        margin-top: 0.5em;
	}
    td.fancy {
        color: #f60;
        background: #666;
	}
    input[type="button"]{
        width:120px;
        margin-left:35px;
        display:block;
        font-family: Verdana, Arial;
    }
    [lang|=en] { 
        color:red; 
    }
```

## CSS样式


### 背景属性
```css
    p {
        background-color: gray;
        padding:20px ;
        margin:2px;
        background-image: url(image_url);
        background-repeat: repeat-y/no-repeat/repeat-x;
        background-position:center/50px 100px/66% 33%;
        background-attachment:fixed/scroll; /* 是否随屏幕滚动 */
    }
```

### 文本属性

```css
    p{
        text-indent: 5em/-5em; /*缩进  */
        text-align:center/justify;
        word-spacing: 30px;
        letter-spacing: -0.5em;
        text-transform: none/uppercase/lowercase/capitalize;
        text-decoration: none/underline/overline/line-through/blink;
        white-space: normal/pre/nowrap/pre-wrap/pre-line;
        unicode-bidi:ltr/rtl;
    }
```
### 字体属性

```css
    body {
        font-family: sans-serif/serif/monospace/cursive/fantasy;
        font-family: Georgia, serif; /*not found Georgia using serif */
        font-style:normal/italic/oblique;
        font-variant:small-caps;
        font-weight:normal/bold/900;
        font-size:60px/3.5em;
    }
```
### 链接样式
```css
    a:link /* 未被访问的链接 */
    a:visited /* 已被访问的链接 */
    a:hover /* 鼠标指针移动到链接上 必须位于 a:link 和 a:visited 之后*/
    a:active /* 正在被点击的链接 必须位于 a:hover 之后*/
```

### 列表属性
```css
    ul {
        list-style-type : square ;
        list-style-image : url(xxx.gif) ;
    }
```
### 表格属性
```css
    table{
        border-collapse:collapse; /* 折叠边框 */
        border-spacing:10px 50px;
        caption-side:top/bottom/inherit;
        empty-cells:hide/show;
        border: 1px solid blue;
        vertical-align:bottom;
        table-layout:fixed/inherit/auto;
    }
``` 
### 框模型

![框模型][img1]

### 定位
```css
    p{
        position:static/relative/absolute/fixed;
        top/bottom:10px;
        left/right:20px;
        overflow:scroll/hidden/visible/auto/inherit;
    }
```

### @media
```css
    @media screen{ 
        /* 显示在屏幕上时的样式 */
        /* 还有all/aural/braille/embossed
        /handheld/print/projetion/tty/tv */
        p.test {
            font-family:verdana,sans-serif;
            font-size:14px
            }
    }
    
```

## CSS3

得到了新的属性支持，支持动画，渐变特效，阴影等属性，多列等新功能

## conference

[W3 School](http://www.w3school.com.cn/css/css_jianjie.asp)

[img1]:data:image/gif;base64,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
