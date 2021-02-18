# *学习笔记*
----------

# print() 语法

1. print语法数字不加引号，其他要加单引号，数字可以直接进行逻辑运算
2. print语法中(其实整个语言)不允许出现中文字符，否则会报错


> #简单示例<br>
print(3+56)<br>
print('hello')<br>
print("hello")

> #数据输出到文件<br>
shuchu=open('D:/SHUCHU.TXT','a+')<br>
print('Hello world',file=shuchu)<br>
shuchu.close()

> #不换行输出<br>
print('hello','world','i fuck you!','now tiem is:',11+5)

> #重复输出<br>
print('重复输出的内容' * 10) # * 10 代表输出十次



# 变量

1. 变量名 = 变量值
2. 变量值可以是数字，字符……
3.变量名与变量名可以用来做运算（均必须是int型）

> #变量名——变量值（数字，可以是整数也可以是小数）<br>
yourdiv = 114514 <br>
print(yourdiv)

> #变量名——变量值<br>
div2 = 'i am py'<br>
print(div2)

> #变量名——变量名（最后会输出后者的值，即114514）<br>
div3 = yourdiv<br>
print(div3)

> #显然也可以用变量名来做运算<br>
div4 = 514<br>
print(yourdiv - div4) #即114514-514=11400

> #input输入，用变量存储<br>
name = input("what 's your name? ")  #将键盘输入的内容存储为name变量<br>
print("ok,you name is: "  + name)   #输出结果会显示“ok,you name is: '输入的名字' ”

> #输出当前时间<br>
import datetime  <br>
NT= datetime.datetime.now()  #获得当前时间，但这是时间数组格式<br>
NT2 = NT.strftime("%Y-%m-%d %H:%M:%S")  #将变量NT的时间值转换为指定的格式<br>
print(NT)  #默认时间戳<br>
print(NT2) #规定的时间格式


> #输出年龄（给予变量类型定义）（int整数型 float浮点小数型）<br>

    NT3 = NT.strftime("%Y")   #承接结合上面的输出时间 
    nowtime = int(NT3)        #赋予类型可以提前在运算式前赋予
    brith_year = input("你什么年份出生？（输入阿拉伯数字）：  ") #用户在此输入的内容将被记录到brith_year变量
    age = nowtime - int(brith_year)    #int将字符串转换成数字型，否则下面无法输出，因为数字型无法与字符串运算
    print(“ok，你今年:” , age)
    
    #也可以这样写，提前将要输入input的内容处理为数字型<br>
    brith_year = int(input("你什么年份出生？（输入阿拉伯数字）：  "))<br>
    后文则只需要：age = nowtime - brith_year #只改变上面这一行代码的情况下<br>
    print("ok,你今年:" , age)  #输出年龄


> #变量三引号多行输出<br>

    example = '''
    这是一个，
    可以…

    多行的

    变量
    '''
    print(example)  #包括空行在内均会被输出
    
# 索引

当以A为起点从左往右时，索引对应 ABCD E————012345，是的，空格也是计入的
当从A为起点从右往左时，索引对应 ABCD E————0 -5 -4 -3 -2 -1

    索引 = 'ABCD E'
    print(索引[0])
    print(索引[4])
    print(索引[-1])
    
    #如果将[]内定义区间（例如1:3），则会输出区间内所有内容,但会排除3这个索引，即不输出D
    print(索引[1:3])    #输出结果为BC
    print(索引[1:-3])   #输出结果为BC（注意，定义的是区间，而不是方向！所以[1:-3]实际上就是[1:3]）
    
    #如果不定义区间，则任何一边不被定义的区间将直接输出到最后一个字符，如果两边都不被定义，则完整输出变量所有内容
    print(索引[1:])  #输出BCD E
    print(索引[:3])  #输出ABC
    print(索引[:])   #输出ABCD E
    #同样的，我们可以再设置一个变量来输出
    全索引 = 索引[:]
    print(全索引)    #输出ABCD E
    
# 格式化字符串 “f”
基本用法 f'{}{}'
    name = 'skt have a new loler'
    last = 'uzi'
    word = f'{name} he is [{last}]' #注意[]是包在{last}外面的
    print(word)
    #skt have a new loler he is [uzi]
    
# 计算字符串数量 len函数
空格和标点也计入

    how_many = 'wor ds!'
    print(len(how_many))
    
    #同样可以配合input计算外部文字
    how_many = 'wor ds!'
    print(len(how_many))
    test = input('输入要计算的文字')    #不计算除了第一行外的内容字符数
    print(len(test))
    
# 方法
只对字符串有效的函数叫做方法
upper方法，转换大写
lower方法，转换小写

    method = "this's method example"
    print(method.upper())
    #输出结果THIS'S METHOD EXAMPLE
    
    print(method.lower())
    #输出结果this's method example
    
