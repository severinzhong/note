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

    ## isinstance(obj,Iterable) 判断obj是否可以迭代
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
    (x ,y ) = map(int , input.split())
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

## 高级内建函数
    retarr = map(func , argarr)
    ret = reduce(func, arr) ## = func(func(arr[0],arr[1]),arr[2])...

# 常用模块

## 正则表达式re模块

需要先`import re`载入re模块,基本规则如下：

|模式|含义|
|:--:|:--|
|精确字符|精确匹配该字符|
|\d|匹配一个数字digit|
|\w|匹配一个数字或字母|
|.|匹配任意字符|
|\s|匹配一个空白符（空格，tab等）|
|\特殊字符|进行转义进行精确匹配,也可以使用r'pattern'|
|[字符集合]|表示在集合内部精确匹配|
|^|表示行的开头（^/d表示数字开头）|
|\A|表示在整个字符串的开头需要匹配|
|$|表示行的结尾|
|\Z|表示整个字符串的结尾|
|\||在[]中表示或|
|\b|表示词边界，被\b包围的部分周围要有空格，且属于[a-zA-Z]|
|\有含义小写的大写|他们的补集|
|{n}|表示n个字符|
|{n，m}|表示n到m个字符|
|*|表示人意长度字符，包括0|
|+|表示至少一个|
|？|表示0或1个，也可以用来防止贪婪匹配(加在后面表示找到最下小的匹配串)|
|（）|在pattern中进行分组,使用group()|
|\number|相同的number个重复|

基本操作如下：

    import re
    m = re.match(pattern,str)
    re.search() ##找到第一个匹配的子串
    re.split(pattern)
    re.sub() ## 找到所有匹配的字串并用另一个字符串代替，subn会返回字符串同时返回替换的数量
    m.group(i) ##0为原始串，1，2，3为括号分组 
    m.start() ##返回匹配的开始位置
    m.end() ##返回匹配的结束位置
    m.span() ##返回开始和结束的位置
    repattern = re.complie(pattern) ##预编译
    repattern.match(str).groups() 
    re.findall(pattern,) ## 返回找到的所有匹配的子串,
    re.finditer() ## 返回找到的所有匹配的字串的iterator

***
参考[python HOWTO](https://docs.python.org/3/howto)

## 科学计算

基本模块包含`numpy,scipy,matplotlib`

### 矩阵计算numpy

一般使用`import numpy as np`来使用

基本操作

    ## type = ndarray
    a = np.arange(15).reshape(3,5) 
    ## a = [[0 1 2 3 4],[5,6,7,8,9],[10,11,1,2,13,14]]
    a.shape ## or shape(a) = (3,4)
    a.ndim  ## or ndim(a) = 2
    a.dtype.name ## int64
    a.itemsize ## 8
    a.size  ## 15

生成矩阵

    a = np.array([1,2,3])
    b = np.array([(1,2,3),(4,5,6)]) ##is also right
    c = np.zeros((3,4))
    d = np.ones((5,4),dtype = np.int16)
    e = np.empty((1,4))
    f = np.arange(10,30,5) ## = [10,15,20,25]
    g = np.linspace(0,2,9) ## = [0, 0.25, 0.5, 0.75, 1,...2]
    print( a ) 
    ## print all use np.set_printoption(threshold='nan')

矩阵运算

    a = np.array([20,30,40,50])
    b = np.arange(4)
    c = a-b
    b**2 ## [0, 1, 4, 9]
    10*np.sin(a)  
    a<35  ## [true,true,false,false]
    
    A = np.array([[1,1],
                  [0,1]])
    B = np.array([[2,0],
                  [3,4]])
    A*B 
    A.dot(B)  ## = np.dot(A,B)
    np.exp([1,2,3]*1 j)  ## 1 j is a complex number 1+j
    a = np.floor(np.random.random((2,3)))
    a.sum() ## all
    a.sum(axis=1)  ## 每列求和
    a.min()
    a.max()
    np.sqrt(A)
    np.add(A,B)
    a = np.fromfunction(func,(5,4))
    np.trace(a)  ## a的迹
    np.linalg.det(a)  ## a的行列式的值
    np.linalg.rank(a)  ## a的秩
    np.linalg.eig(a)  ## a的本征值
    np.linalg.svd(a)  ## a的奇异值分解

    a[1,2,...] ## = a[1,2,:,:,:]
    for row in b :
        code
    for element in b.flat :
        code
    a.ravel()  ## => a=a.flat
    a.T  ##转置
    a.resize((2,6))  ## => a=a.reshape((2,6))

    np.vstack(a,b) ## 竖着拼接两个矩阵
    np.hstack(a,b) ## 横着拼接两个矩阵
    np.column_stack()
    np.r_[1*4,0,4]  ## = [1,2,3,0,4]
    np.hsplit(a,3) ## 横着拆成3个矩阵
    np.vsplit(a,3)
    np.array_split()
    c = a.view() ## c.base is a , c not is a
    d = a.copy()

随机模块

    import numpy.random as random
    random.seed(42)
    random.rand(1,3)
    random.random((3,3))  ## [0,1)
    random.uniform(1,6,10)  ## 10 numbers from [1,6)
    random.randint(1,6,10)
    random.normal(size=(5,2))  ## 2*5的正态分布
    random.binomial(n=5,p=0.5,size=5)  ## 5个二项式分布
    

### 绘图matplotlib
>`from matplotlib import pyplot as plt`来使用库函数

>一张图（figure）包含一个画板（axes），包含一套坐标系（axis）和一些注释

下面是一张图的示例：

    x = np.linespace(0,2,100)
    plt.plot(x,x,label='liner')  
    # x.shape : (1000,1)is right,(1,1000) is wrong
    plt.plot(x,x**2,label='quadratic')
    plt.xlabel('x label')
    plt.ylabel('y label')
    plt.title('simple plot')
    plt.legend()  ##图例
    plt.show()

>`plot`的调控参数有颜色`r,b,g,...`, 线的形状`-,--,...`, 点的形状`o,*,s,^,...` ,例如`'bs','r--'`

下面是绘制点分布图

    data = { 'a':np.arange(50)
             'c':np.random.randit(0,50,50),
             'd':np.random.randn(50)
    }
    data['b'] = data['a'] + 10*np.random.randn(50)
    data['d'] = np.abs(data['d']) * 100

    plt.scatter('a','b','c'=c,s='d',data=data)
    plt.show()

制作一张直方图

    mu, sigma = 100, 15
    x = mu + sigma* np.random.randn(100000)
    n,bins,patches = plt.hist(x,50,normed=1,facecolor='g',alpha=0.75)
    plt.text(60,0.025,r'$\mu=100,\\sigma=15$')
    plt.axis([40,160,0,0.03])
    plt.grid(True)
    plt.show()

一些控制和操作
 
    #子图绘制
    fig, (ax1,ax2) = plt.subplots(1,2)
    ax1.plot(x1,y1)
    ax2.plot(x2,y2)
    plt.show()

    plt.figure(1)
    plt.subplot(221)
    #do sth
    plt.subplot(222)
    #do sth
    plt.subplot(223)
    #do sth
    plt.subplot(224)
    #do sth
    plt.gca().yaxis.set_minor_formatter(NullFormatter())
    plt.subplots_adjust(top=0.92,buttom=0.08,left=0.10,right=0.95,hspace=0.25,wspace=0.35)
    plt.show()

***
参考[matplotlib.org](https://matplotlib.org)


