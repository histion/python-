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
NT3 = NT.strftime("%Y") #承接结合上面的输出时间 <br>
nowtime = int(NT3) #赋予类型可以提前在运算式前赋予<br>
brith_year = input("你什么年份出生？（输入阿拉伯数字）：  ")<br>
age = nowtime - int(brith_year) #int将字符串转换成数字型，否则下面无法输出，因为数字型无法与字符串运算<br>
>>#也可以这样写，提前将要输入input的内容处理为数字型<br>
>>brith_year = int(input("你什么年份出生？（输入阿拉伯数字）：  "))<br>
>>后文则只需要：age = nowtime - brith_year #只改变上面这一行代码的情况下<br>
>print("ok,你今年:" , age)  #输出年龄
