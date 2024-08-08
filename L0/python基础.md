# Chapter2: Python基础
## 2.1 Python基础语法
python标识符(变量名，函数名)命名要求：
* 标识符须要由字母，数字和下划线组成
* 首字符必须是字母或者下划线_
* 标识符对大小写敏感
* 标识符不能与python关键字重名

以下代码可以查看python的关键词（保留字符）


```python
import keyword
print(keyword.kwlist)
```

    ['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
    
## 2.2 基本数据类型

python基本数据类型:
* 数字Number
    * int整数
    * float浮点数
    * complex复数
* 布尔型bool
* 列表list
* 元组tuple
* 集合set
* 字典Dictionary

可以修改的是：列表list，集合set，字典Dictionary

不可以修改的是：数字Number，布尔型bool，元组tuple


```python
a,b = 1,2 #另一种单行赋值的方式

#下面让我们来看看各种类型的数据长什么样
t_int = 1 #整数
t_float = 1.0 #浮点数
t_complex = 1.2j #复数
t_bool = True #布尔类型
t_list = [1,1,3,3,5,5] #列表
t_tuple = (1,1,3,3,5,5) #元组
t_set = {1,3,5} #集合
t_dict = {'day':18,'month':6,'year':2024} #字典

print(" t_int的类型是：",type(t_int),' t_int的值是: ',t_int)
print(" t_float的类型是：",type(t_float),' t_float的值是: ',t_float)
print(" t_complex的类型是：",type(t_complex),' t_complex的值是: ',t_complex)
print(" t_bool的类型是：",type(t_bool),' t_bool的值是: ',t_bool)
print(" t_list的类型是：",type(t_list),' t_list的值是: ',t_list)
print(" t_tuple的类型是：",type(t_tuple),' t_tuple的值是: ',t_tuple)
print(" t_set的类型是：",type(t_set),' t_set的值是: ',t_set)
print(" t_dict的类型是：",type(t_dict),' t_int的值是: ',t_dict)
```

     t_int的类型是： <class 'int'>  t_int的值是:  1
     t_float的类型是： <class 'float'>  t_float的值是:  1.0
     t_complex的类型是： <class 'complex'>  t_complex的值是:  1.2j
     t_bool的类型是： <class 'bool'>  t_bool的值是:  True
     t_list的类型是： <class 'list'>  t_list的值是:  [1, 1, 3, 3, 5, 5]
     t_tuple的类型是： <class 'tuple'>  t_tuple的值是:  (1, 1, 3, 3, 5, 5)
     t_set的类型是： <class 'set'>  t_set的值是:  {1, 3, 5}
     t_dict的类型是： <class 'dict'>  t_int的值是:  {'day': 18, 'month': 6, 'year': 2024}
    q
