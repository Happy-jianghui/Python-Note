#   Python总结（防止忘记）

##  String
  Python 中的字符串有两种索引方式，**从左往右以 0 开始，从右往左以 -1 开始**。  
  **eg:  
  Str = "abcdef"**    
  从左往右的字符串 
  |Str|a|b|c|d|e|f|
  |:---:|:--:|:---:|:---:|:---:|:---:|:---:|
  |从左往右索引|0|1|2|3|4|5|
  
  从右往左的字符串 
  |Str|a|b|c|d|e|f|
  |:---:|:--:|:---:|:---:|:---:|:---:|:---:|
  |从右往左索引|-6|-5|-4|-3|-2|-1|  
  ___
  字符串的截取的语法格式如下：**变量[头下标:尾下标:步长]**
  Str = "abcdef"  
  print(str[2:5:1])
  >输出结果：cde  
  
## Print输出
   print 默认输出是换行的，如果要实现不换行需要在变量末尾加上 end=""
   >print(x, end=" ")  
   
## Python基本数据类型
  ### 多个变量赋值
  同时为多个变量赋值,创建一个整型对象，值为 1，从后向前赋值，三个变量被赋予相同的数
  > a = b = c = 1  

  多个对象指定多个变量赋值,两个整型对象 1 和 2 的分配给变量 a 和 b，字符串对象 "abc" 分配给变量 c
  > a, b, c = 1, 2, 'abc'
  ### 数值运算
  数值的除法包含两个运算符：/ 返回一个浮点数，// 返回一个整数。
 
## Python3 函数
 函数是组织好的，可重复使用的，用来实现单一，或相关联功能的代码段。
 函数能提高应用的模块性，和代码的重复利用率。你已经知道Python提供了许多内建函数，比如print()。但你也可以自己创建函数，这被叫做用户自定义函数。
 ### 定义一个函数
 - 函数代码块以 def 关键词开头，后接函数标识符名称和圆括号 ()。
 - 任何传入参数和自变量必须放在圆括号中间，圆括号之间可以用于定义参数。
 - 函数的第一行语句可以选择性地使用文档字符串—用于存放函数说明。
 - 函数内容以冒号 : 起始，并且缩进。
 - return [表达式] 结束函数，选择性地返回一个值给调用方，不带表达式的 return 相当于返回 None。
  ![image](https://user-images.githubusercontent.com/98568967/221125950-4abb6b5a-f4c2-44da-ae90-662b2daf9f39.png)  
    
  ### 函数调用
  定义一个函数：给了函数一个名称，指定了函数里包含的参数，和代码块结构。  
  这个函数的基本结构完成以后，你可以通过另一个函数调用执行，也可以直接从 Python 命令提示符执行。
  
 ## Python数据结构
  ### 遍历技巧
    在序列中遍历时，索引位置和对应值可以使用 enumerate() 函数同时得到：  
     ``` Python
      for i, v in enumerate(['tic', 'tac', 'toe']):
          print(i, v)   
     ```
     输入结果：
      0 tic
      1 tac
      2 toe
  
    同时遍历两个或更多的序列，可以使用 zip() 组合：  
    ``` Python
      questions = ['name', 'quest', 'favorite color']
      answers = ['lancelot', 'the holy grail', 'blue']
      for q, a in zip(questions, answers):
          print('What is your {0}?  It is {1}.'.format(q, a)) 
     ```
     输入结果：
      What is your name?  It is lancelot.
      What is your quest?  It is the holy grail.
      What is your favorite color?  It is blue.
