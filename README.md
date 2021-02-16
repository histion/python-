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
  
> #输出当前时间<br>
import datetime  <br>
NT= datetime.datetime.now()  #获得当前时间，但这是时间数组格式<br>
NT2 = NT.strftime("%Y-%m-%d %H:%M:%S")  #转换为指定的格式<br>
print(NT)  #默认时间戳<br>
print(NT2) #规定的时间格式

# 标题
