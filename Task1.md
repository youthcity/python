
### 1.环境搭建

#### Anaconda环境配置
![peizhi.jpg](attachment:peizhi.jpg)  
之后就可以打开命令行(最好用管理员模式打开) 输入 conda --version  
如果输出conda （版本号）之类的就说明环境变量设置成功了.  
之后与pycharm进行连接。  

#### 解释器
采用pycharm编辑器，同时使用jupyter进行码代码及做笔记。

### 2.python初体验

#### print and input


```python
1 + 2
```




    3




```python
1
```




    1




```python
print("hello Python world!")
```

    hello Python world!
    


```python
message = "hello Python world!"
print(message)
```

    hello Python world!
    

### 3.python 基础讲解

#### python变量特征+命名规则

Python 是弱类型语言，弱类型语言有两个典型特征：

    变量无须声明即可直接赋值：对一个不存在的变量赋值就相当于定义了一个新变量。
    变量的数据类型可以动态改变：同一个变量可以一会儿被赋值为整数值，一会儿被赋值为字符串。

在Python中使用变量，须遵守：

    变量名只能包含字母、数字和下划线，变量不能以数字开头。
    Python变量区分大小写
    不能将Python关键字用作变量名
    Python跟踪所有的值，并自动删除不再有变量指向的值，这称为垃圾收集

#### 注释方法

1. 单行注释

Python编程语言的单行注释以#开头，单行注释可以作为单独的一行放在被注释代码行之上，也可以放在语句或者表达式之后。

2. 多行注释

Python编程语言的多行注释在注释行上下分别加'''或"""。


```python
#注释
1+2
```




    3




```python
1+2#注释
```




    3




```python
"""
这是多行注释
这是多行注释
"""
1+2
```




    3




```python
'''
这是多行注释
这是多行注释
'''
1+2
```




    3



#### 学会使用dir()及help()

##### dir()

dir()用来查询一个类或者对象所有属性，比如：


```python
dir(list)
```




    ['__add__',
     '__class__',
     '__contains__',
     '__delattr__',
     '__delitem__',
     '__dir__',
     '__doc__',
     '__eq__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__getitem__',
     '__gt__',
     '__hash__',
     '__iadd__',
     '__imul__',
     '__init__',
     '__init_subclass__',
     '__iter__',
     '__le__',
     '__len__',
     '__lt__',
     '__mul__',
     '__ne__',
     '__new__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__reversed__',
     '__rmul__',
     '__setattr__',
     '__setitem__',
     '__sizeof__',
     '__str__',
     '__subclasshook__',
     'append',
     'clear',
     'copy',
     'count',
     'extend',
     'index',
     'insert',
     'pop',
     'remove',
     'reverse',
     'sort']



##### help()
函数帮助我们了解模块、类型、对象、方法、属性的详细信息  
1. 帮助查看类型详细信息，包含类的创建方式、属性、方法


```python
help(list)
```

    Help on class list in module builtins:
    
    class list(object)
     |  list(iterable=(), /)
     |  
     |  Built-in mutable sequence.
     |  
     |  If no argument is given, the constructor creates a new empty list.
     |  The argument must be an iterable if specified.
     |  
     |  Methods defined here:
     |  
     |  __add__(self, value, /)
     |      Return self+value.
     |  
     |  __contains__(self, key, /)
     |      Return key in self.
     |  
     |  __delitem__(self, key, /)
     |      Delete self[key].
     |  
     |  __eq__(self, value, /)
     |      Return self==value.
     |  
     |  __ge__(self, value, /)
     |      Return self>=value.
     |  
     |  __getattribute__(self, name, /)
     |      Return getattr(self, name).
     |  
     |  __getitem__(...)
     |      x.__getitem__(y) <==> x[y]
     |  
     |  __gt__(self, value, /)
     |      Return self>value.
     |  
     |  __iadd__(self, value, /)
     |      Implement self+=value.
     |  
     |  __imul__(self, value, /)
     |      Implement self*=value.
     |  
     |  __init__(self, /, *args, **kwargs)
     |      Initialize self.  See help(type(self)) for accurate signature.
     |  
     |  __iter__(self, /)
     |      Implement iter(self).
     |  
     |  __le__(self, value, /)
     |      Return self<=value.
     |  
     |  __len__(self, /)
     |      Return len(self).
     |  
     |  __lt__(self, value, /)
     |      Return self<value.
     |  
     |  __mul__(self, value, /)
     |      Return self*value.
     |  
     |  __ne__(self, value, /)
     |      Return self!=value.
     |  
     |  __repr__(self, /)
     |      Return repr(self).
     |  
     |  __reversed__(self, /)
     |      Return a reverse iterator over the list.
     |  
     |  __rmul__(self, value, /)
     |      Return value*self.
     |  
     |  __setitem__(self, key, value, /)
     |      Set self[key] to value.
     |  
     |  __sizeof__(self, /)
     |      Return the size of the list in memory, in bytes.
     |  
     |  append(self, object, /)
     |      Append object to the end of the list.
     |  
     |  clear(self, /)
     |      Remove all items from list.
     |  
     |  copy(self, /)
     |      Return a shallow copy of the list.
     |  
     |  count(self, value, /)
     |      Return number of occurrences of value.
     |  
     |  extend(self, iterable, /)
     |      Extend list by appending elements from the iterable.
     |  
     |  index(self, value, start=0, stop=9223372036854775807, /)
     |      Return first index of value.
     |      
     |      Raises ValueError if the value is not present.
     |  
     |  insert(self, index, object, /)
     |      Insert object before index.
     |  
     |  pop(self, index=-1, /)
     |      Remove and return item at index (default last).
     |      
     |      Raises IndexError if list is empty or index is out of range.
     |  
     |  remove(self, value, /)
     |      Remove first occurrence of value.
     |      
     |      Raises ValueError if the value is not present.
     |  
     |  reverse(self, /)
     |      Reverse *IN PLACE*.
     |  
     |  sort(self, /, *, key=None, reverse=False)
     |      Stable sort *IN PLACE*.
     |  
     |  ----------------------------------------------------------------------
     |  Static methods defined here:
     |  
     |  __new__(*args, **kwargs) from builtins.type
     |      Create and return a new object.  See help(type) for accurate signature.
     |  
     |  ----------------------------------------------------------------------
     |  Data and other attributes defined here:
     |  
     |  __hash__ = None
    
    

2. 帮助查看方法的详细使用信息（使用时要注意输入完整路径，使用模块帮助时，需要先导入模块）  

举例如下：

查看python所有的关键字：help("keywords")

查看python所有的modules：help("modules")

单看python所有的modules中包含指定字符串的modules： help("modules yourstr")

查看python中常见的topics： help("topics")

查看python标准库中的module：import os.path + help("os.path")

查看python内置的类型：help("list")

查看python类型的成员方法：help("str.find") 

查看python内置函数：help("open")

#### import使用
1. module  
通常模块为一个文件，直接使用import来导入就好了。可以作为module的文件类型有".py"、".pyo"、".pyc"、".pyd"、".so"、".dll"。

2. package  
通常包总是一个目录，可以使用import导入包，或者from + import来导入包中的部分模块。包目录下为首的一个文件便是 __init__.py。然后是一些模块文件和子目录，假如子目录中也有 __init__.py 那么它就是这个包的子包了。


#### pep8 介绍
pep8 即Python的一些代码风格的要求。  
 
##### 代码布局  

缩进

    使用4个空格作为一个缩进层次
    当需要换行时，续行应该和所包含的元素垂直对齐或者使用悬垂缩进，也就是第一行不应该有任何参数，续行也应该有缩进来明确其作为一个续航。
    列表元素之类的需要后括号结束的，后括号要么和元素对齐要么顶格
  
最大行长度

    对于所有行来说，最长79字符
    对于文档字符串或者注释，最长72字符
    太长的就用backslash换行处理，换行规则之前已经说过了

空行

    顶层函数以及类定义和其他部分用两个空行隔开
    类之内的方法定义之间用一个空行隔开
    对于一组相关的函数和其他之间可以有额外的空行
    可以使用空行来区分逻辑块

源代码编码

    py3使用utf-8，py2使用ascii
    py3已经使用utf-8, py2已经使用ascii的源代码不应该有编码声明


import相关

    各个import独立成行
    import应该总是在文件的最上面，在模块注释和文档字符串之后，在模块变量和常量之前
    注意import的顺序，各个import的组需要用空行隔开，顺序为:
    

 - 标准库import
 - 相关的第三方import
 - 本地应用和库的import
    
其他的建议

    一行的尾部不要有空格
    二元运算符前后始终都最好有一个空格
    在一个表达式中有不同优先级的运算符，可以添加空格以区别优先级
    在调用函数时作为参数的那个等号则前后不要有空格（虽然看起来像个二元运算符）,比如func(a=3, b=4)而不是func(a = 3, b = 4)
    带箭头的函数，箭头两端也应该和二元运算符一样，前后有空格def func() -> AnyStr: ...
    函数声明的默认参数，只有在有notation的时候前后有等号，否则前后没有等号
    

### 4. pyhon 数值基本知识

基本数据类型

1、数字  ---> int类

　　    当然对于数字，Python的数字类型有int整型、long长整型、float浮点数、complex复数、以及布尔值（0和1），这里只针对int整型进行介绍学习。

　　　　在Python2中，整数的大小是有限制的，即当数字超过一定的范围不再是int类型，而是long长整型，而在Python3中，无论整数的大小长度为多少，统称为整型int。

　　　　其主要方法有以下两种：

　　　　int -->将字符串数据类型转为int类型,  注：字符串内的内容必须是数字　

　　　　bit_length() -->将数字转换为二进制，并且返回最少位二进制的位数


 
2、布尔值  --->bool类

　　　  对于布尔值，只有两种结果即True和False，其分别对应与二进制中的0和1。而对于真即True的值太多了，我们只需要了解假即Flase的值有哪些---》None、空（即 [ ]/( ) /" "/{ }）、0；


3、字符串  --->str类

　　　     关于字符串是Python中最常用的数据类型，其用途也很多，我们可以使用单引号 ‘’或者双引号“”来创建字符串。

　　　　   字符串是不可修改的。所有关于字符我们可以从 索引、切片、长度、遍历、删除、分割、清除空白、大小写转换、判断以什么开头等方面对字符串进行介绍。
   
4、列表  --->list类

　　　　列表是由一系列特定元素顺序排列的元素组成的，它的元素可以是任何数据类型即数字、字符串、列表、元组、字典、布尔值等等，同时其元素也是可修改的。
    
5、元组  --->tuple类

　　　　元组即为不可修改的列表。其于特性跟list相似。其使用圆括号而不是方括号来标识。 
    
    
6、字典  --->dict类

　　　 字典为一系列的键-值对，每个键值对用逗号隔开，每个键都与一个值相对应，可以通过使用键来访问对应的值。无序的。

　　　　键的定义必须是不可变的，即可以是数字、字符串也可以是元组，还有布尔值等。

　　　　而值的定义可以是任意数据类型。    
    
    
7、集合 -->set类

　　　   关于集合set的定义：在我看来集合就像一个篮子，你可以往里面存东西也可往里面取东西，但是这些东西又是无序的，你很难指定单独去取某一样东西；同时它又可以通过一定的方法筛选去获得你需要的那部分东西。故集合可以 创建、增、删、关系运算。    
    
    
    

比较运算：  
![1.png](attachment:1.png)

赋值运算：  
![2.png](attachment:2.png)

逻辑运算：  
![3.png](attachment:3.png)

成员运算：  
![4.png](attachment:4.png)

身份运算：  
![5.png](attachment:5.png)

运算符优先级：  
![youxianji.jpg](attachment:youxianji.jpg)
