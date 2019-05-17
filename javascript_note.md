# JavaScript NoteBook

## 变量和数据类型
```js
    var a , x =  2 ;
    var y = x + 3.2 ;
    var answer = "No" ;
    var cars=new Array();
    var cars=new Array("Audi","BMW","Volvo");
    var cars=["Audi","BMW","Volvo"];
    cars[0] = "Volvo" ;

    var person={
        firstname : "Bill",
        lastname  : "Gates",
        id        :  5566
        };
    name=person.lastname;
    name=person["lastname"];
    person=null;
```

## 语法和函数
```js
if () {} else {}

if () {} else if () {} else {}

switch (n){
    case 1 : break ;
    default :
}

for (var i=0;i<cars.length;i++){}

for (x in person){}

while(){}

do{}while();

try{}
catch(err){}

throw "string" ;

function functionname(){}

```

## HTML管理

* 能够改变页面中的所有 HTML 元素
* 能够改变页面中的所有 HTML 属性
* 能够改变页面中的所有 CSS 样式
* 能够对页面中的所有事件做出反应
```js
    ducoment.getElementById().innerHTML = 'new things' ;
    ducoment.getElementByClass().style.fontSize = "14px" ;
    ducoment.getElementByTagName().src="landscape.jpg"
    document.getElementById("myBtn").onclick=function(){displayDate()};

    var para=document.createElement("p");
    var node=document.createTextNode("这是新段落。");
    para.appendChild(node);

    var element=document.getElementById("div1");
    element.appendChild(para);

    var parent=document.getElementById("div1");
    var child=document.getElementById("p1");
    parent.removeChild(child);
```
基本事件表如下：

|事件|解释|
|:--|:--|
|onclick | 点击事件
|onload | 进入页面
|onunload | 离开页面
|onchange | 改变输入字段
|onmouseover | 鼠标到达
|onmouseout | 鼠标离开
|onmousedown | 点下鼠标
|onmouseup | 释放鼠标
|onmousemove | 鼠标移动
|onfocus | 获得焦点
|onblur | 失去焦点
|ondblclick | 双击事件
|onkeydown |  某个按键被按下 event.keyCode(IE)/event.which(Others)
|onkeyup | 某个按键松开
|onkeypress | 某个按键按下且松开

事件属性如下:

|属性|解释|
|:--|:--|
|altKey	|返回当事件被触发时，"ALT" 是否被按下。
|button	|返回当事件被触发时，哪个鼠标按钮被点击。
|clientX	|返回当事件被触发时，鼠标指针的水平坐标。
|clientY	|返回当事件被触发时，鼠标指针的垂直坐标。
|ctrlKey	|返回当事件被触发时，"CTRL" 键是否被按下。
|metaKey	|返回当事件被触发时，"meta" 键是否被按下。
|relatedTarget	|返回与事件的目标节点相关的节点。
|screenX	|返回当某个事件被触发时，鼠标指针的水平坐标。
|screenY	|返回当某个事件被触发时，鼠标指针的垂直坐标。
|shiftKey	|返回当事件被触发时，"SHIFT" 键是否被按下。
|bubbles	|返回布尔值，指示事件是否是起泡事件类型。
|cancelable	|返回布尔值，指示事件是否可拥可取消的默认动作。
|currentTarget	|返回其事件监听器触发该事件的元素。
|eventPhase	|返回事件传播的当前阶段。
|target	|返回触发此事件的元素（事件的目标节点）。
|timeStamp	|返回事件生成的日期和时间。
|type	|返回当前 Event 对象表示的事件的名称。
|cancelBubble	|如果事件句柄想阻止事件传播到包容对象，必须把该属性设为 true。
|fromElement	|对于 mouseover 和 mouseout 事件，fromElement 引用移出鼠标的元素。
|keyCode	|对于 keypress 事件，该属性声明了被敲击的键生成的 Unicode 字符码。对于 keydown 和 keyup 事件，它指定了被敲击的键的虚拟键盘码。虚拟键盘码可能和使用的键盘的布局相关。
|offsetX,offsetY	|发生事件的地点在事件源元素的坐标系统中的 x 坐标和 y 坐标。
|returnValue	|如果设置了该属性，它的值比事件句柄的返回值优先级高。把这个属性设置为 fasle，可以取消发生事件的源元素的默认动作。
|srcElement	|对于生成事件的 Window 对象、Document 对象或 Element 对象的引用。
|toElement	|对于 mouseover 和 mouseout 事件，该属性引用移入鼠标的元素。
|x,y	|事件发生的位置的 x 坐标和 y 坐标，它们相对于用CSS动态定位的最内层包容元素。

## conference

[W3 School](http://www.w3school.com.cn/js/js_intro.asp)
