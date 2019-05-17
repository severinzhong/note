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

![框模型](http://www.w3school.com.cn/i/ct_boxmodel.gif)

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
