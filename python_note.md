# python基础
## 变量
    ## basic
    num = 9 + 1 
    bool = a>0 and b==c or not d!=9
    bool = obj in arr
    ## string
    str = "hello world"
    str.find('o')
    str.strip('')  ##去除两边的字符
    strarr = str.split(' ')
    ## list
    arr = list()
    arr = ["one" , "two" , "three"]
    arr[0] = "zero"
    arr[0:3]
    arr.insert(1,"four")
    arr.sort()
    arr2 = sorted(arr)
    arr.append(obj)
    arr.pop(0) ##弹出第一个
    ##set
    s = set()
    ##dict
    s = dict()
    s = {
        "jack":23,
        "lisa":21
    }
    s["tom"] = 6 

## 程序结构

    import module as nickname
    from module import function

    try:
        code
    except errortype:
        error happend
    finally:
        final work

    for obj in arr:
        code

    for iter,value in enumerate(list):
        code

    ## isinstance(obj,Iterable) 判断obj是否可以迭代
    for key,value in dict:  
        code

    for x,y in [(1,1),(2,4),(3,9)] :
        code

    while expr :
        code

    if expr :
        code
    elif expr :
        code
    else :
        code
    
    class name: ##name(list)来派生list操作
        def __init__(self):  ## 初始化函数

    def func():
        code
        return sth

## 标准输入输出
    (x ,y ) = map(int , input.split())
    print(x+y,end="") ##end="" 表示不换行

## 文件输入输出
    import os
    path.exist(url)
    file = open(url,'w') ##w,r,wb,rb,w+...
    with open(url,"w+") as file
        code here (no use close file)
    file.close()
    file.read()
    file.write()
    file.seek() ##返回文件开始
    locals() ## 所有名集合

## 高级函数
    retarr = map(func , argarr)
    ret = reduce(func, arr) ## = func(func(arr[0],arr[1]),arr[2])...

## 正则表达式

需要先`import re`载入re模块,基本规则如下：

|模式|含义|
|:--:|:--|
|精确字符|精确匹配该字符|
|/d|匹配一个数字digit|
|/w|匹配一个数字或字母|
|.|匹配任意字符|
|*|匹配任意长度字符（包括0）|
|/s|匹配一个空白符（空格，tab等）|
|/特殊字符|进行转义进行精确匹配|
|[字符集合]|表示在集合内部精确匹配|
|^|表示行的开头（^/d表示数字开头）|
|$|表示结尾|


后面跟{n}表示n个字符，{n，m}表示n到m个字符，+表示至少一个，？表示0或1个，也可以用来防止贪婪匹配，使用（）在pattern中进行分组

基本操作如下：

    import re
    m = re.match(pattern,atr)
    re.split(pattern)
    m.group(i) ##0为原始串，1，2，3为括号分组 
    repattern = re.complie(pattern) ##预编译
    repattern.match(str).groups() 