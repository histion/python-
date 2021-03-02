# *学习笔记*
----------

# print() 语法

1. print语法数字不加引号，其他要加单引号，数字可以直接进行逻辑运算
2. print语法中(其实整个语言)不允许出现中文字符，否则会报错


> #简单示例
```python
    print(3+56)
    print('hello')
    print("hello")
```
> #数据输出到文件
```python
    shuchu=open('D:/SHUCHU.TXT','a+')
    print('Hello world',file=shuchu)
    shuchu.close()
```
> #不换行输出
```python
    print('hello','world','i fuck you!','now tiem is:',11+5)
```
> #重复输出
```python
    print('重复输出的内容' * 10) # * 10 代表输出十次
```


# 变量

1. 变量名 = 变量值
2. 变量值可以是数字，字符……
3. 变量名与变量名可以用来做运算（均必须是int型）

> #变量名——变量值（数字，可以是整数也可以是小数）
```python
    yourdiv = 114514
    print(yourdiv)
```
> #变量名——变量值
```python
    div2 = 'i am py'
    print(div2)
```
> #变量名——变量名（最后会输出后者的值，即114514）
```python
    div3 = yourdiv
    print(div3)
```
> #显然也可以用变量名来做运算
```python
    div4 = 514
    print(yourdiv - div4) #即114514-514=11400
```
> #input输入，用变量存储
```python
    name = input("what 's your name? ")  #将键盘输入的内容存储为name变量
    print("ok,you name is: "  + name)   #输出结果会显示“ok,you name is: '输入的名字' ”
```
> #输出当前时间
```python
    import datetime  
    NT= datetime.datetime.now()  #获得当前时间，但这是时间数组格式
    NT2 = NT.strftime("%Y-%m-%d %H:%M:%S")  #将变量NT的时间值转换为指定的格式
    print(NT)  #默认时间戳
    print(NT2) #规定的时间格式
```

> #输出年龄（给予变量类型定义）（int整数型 float浮点小数型）<br>
```python
    NT3 = NT.strftime("%Y")   #承接结合上面的输出时间
    nowtime = int(NT3)        #赋予类型可以提前在运算式前赋予
    brith_year = input("你什么年份出生？（输入阿拉伯数字）：  ") #用户在此输入的内容将被记录到brith_year变量
    age = nowtime - int(brith_year)    #int将字符串转换成数字型，否则下面无法输出，因为数字型无法与字符串运算
    print(“ok，你今年:” , age)

    #也可以这样写，提前将要输入input的内容处理为数字型<br>
    brith_year = int(input("你什么年份出生？（输入阿拉伯数字）：  "))<br>
    后文则只需要：age = nowtime - brith_year #只改变上面这一行代码的情况下<br>
    print("ok,你今年:" , age)  #输出年龄
```

> #变量三引号多行输出<br>
```python
    example = '''
    这是一个，
    可以…

    多行的

    变量
    '''
    print(example)  #包括空行在内均会被输出
```
# 索引

当以A为起点从左往右时，索引对应 ABCD E————012345，是的，空格也是计入的<br>
当从A为起点从右往左时，索引对应 ABCD E————0 -5 -4 -3 -2 -1
```python
    索引 = 'ABCD E'
    print(索引[0])
    print(索引[4])
    print(索引[-1])
```
> #如果将[]内定义区间（例如1:3），则会输出区间内所有内容,但会排除3这个索引，即不输出D
```python
    print(索引[1:3])    #输出结果为BC
    print(索引[1:-3])   #输出结果为BC（注意，定义的是区间，而不是方向！所以[1:-3]实际上就是[1:3]）
```
> #如果不定义区间，则任何一边不被定义的区间将直接输出到最后一个字符，如果两边都不被定义，则完整输出变量所有内容
```python
    print(索引[1:])  #输出BCD E
    print(索引[:3])  #输出ABC
    print(索引[:])   #输出ABCD E
    #同样的，我们可以再设置一个变量来输出
    全索引 = 索引[:]
    print(全索引)    #输出ABCD E
```

# 格式化字符串 “f”
基本用法 f'{}{}'
```python
    name = 'skt have a new loler'
    last = 'uzi'
    word = f'{name} he is [{last}]' #注意[]是包在{last}外面的
    print(word)
    #skt have a new loler he is [uzi]
```
# 计算字符串数量 len函数
空格和标点也计入
```python
    how_many = 'wor ds!'
    print(len(how_many))

    #同样可以配合input计算外部文字
    how_many = 'wor ds!'
    print(len(how_many))
    test = input('输入要计算的文字')    #不计算除了第一行外的内容字符数
    print(len(test))
```
# 方法
只对字符串有效的函数叫做方法<br>

> #upper方法，转换大写<br>
> #lower方法，转换小写<br>
> #title方法，首字符大写，如果有空格，则每个空格到另一个空格之间字符串的首字母大写,接在'后面的第一个字母也会大写，其他全部转换为小写
```python
    method = "this's method example"
    print(method.upper())
    #输出结果THIS'S METHOD EXAMPLE
    print(method.lower())
    #输出结果this's method example
    print(method.title())
    输出结果This'S Method Example，马上会变成大写
```
> #find方法，寻找字符/字符串在内容中的索引<br>
```python
    print(method.find('H'))
    print(method.find('s')) #find方法将会对应括号内字母（区分大小写）第一次出现的位置索引
```
> #replace方法，替换字符/字符串，同样区分大小写
```python
method = "tHIs's methoD example"
    print(method.replace('H','I'))
    #输出结果为 tIIs's methoD example
    print(method.replace("HIs's",'I'))
    #输出结果为 tI methoD example
```

# 运算符

> #用in运算符判断字符/串是否在变量中，同样区分大小写
```python
print('example' in method) #得到结果为True，如果没有则是Flase
```


# 算数运算符号
>乘除法——符号对应 *  /
```python
print(5*3)     #单*为乘法运算符
print(10 / 3)   #单/为除法运算
print(10 % 3 )  #输入%会返回除法结果的余数，即10÷3=3余下1
```

>符号复用
```python
print(10.0 // 3)
print(11.9 //3)  #两个//则是取整数,总是只取取整数部分，即：3.101——3.0，3.99——3.0
print(10 ** 3)  #两个*代表第一个数的第二个数次方，即10的三次方——1000
```

>增强型赋值运算符
通常
```python
x = 10
x = x + 3
print(x)   #会得到x=13
```
而增强赋值运算符（+ - * /接上=） 
```python
x = 10
x += 3   #等同与 x = x + 3
print(x)  #结果13
```
