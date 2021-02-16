*#学习笔记*
----------

# print() 语法

1. print语法数字不加引号，其他要加单引号，数字可以直接进行逻辑运算
2. print语法中(其实整个语言)不允许出现中文字符，否则会报错


> #简单示例
  print(3+56)
  print('hello')
  print("hello")

> #数据输出到文件
  shuchu=open('D:/SHUCHU.TXT','a+')
  print('Hello world',file=shuchu)
  shuchu.close()

> #不换行输出
  print('hello','world','i fuck you!','now tiem is:',11+5)
  
# p语法
