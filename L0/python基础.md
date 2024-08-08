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
    #输入Tab缩进可以直接变成代码块


## 2.3 运算符
### 2.3.1 算数运算符
| 运算符 | 描述 |
| --- | --- |
| `+` | 加 |
| `-` | 减 |
| `*` | 乘 |
| `/` | 除 |
| `//` | 整除,只保留整数 |
| `%` | 模运算或者取余数除法,只保留余数 |
| `**` | 幂运算 |


### 2.3.2 比较运算符
| 运算符 | 描述 |
| --- | --- |
| `>` | 大于 |
| `<` | 小于 |
| `>=` | 大于等于 |
| `<=` | 小于等于 |
| `==` | 等于 |
| `!=` | 不等于 |


### 2.3.3 赋值运算符
| 运算符 | 描述 | 等价表达 |
| --- | --- | --- |
| `=` | 基础赋值 | |
| `+=` | 加法赋值 | a+=b等价于 a=a+b |
| `-=` | 减法赋值 | a-=b等价于 a=a-b |
| `*=` | 小于等于 | a*=b等价于 a=a*b |
| `/=` | 等于 | a/=b等价于 a=a/b |
| `//=` | 等于 | a//=b等价于 a=a//b |
| `%=` | 等于 | a%=b等价于 a=a%b |
| `**=` | 等于 | a**=b等价于 a=a**b |


### 2.3.4 逻辑运算符
| 运算符 | 描述 |
| --- | --- |
| `and` | 逻辑与 |
| `or` | 逻辑或 |
| `not` | 逻辑非 |


## 2.4 列表
列表是一个有索引的序列，索引从0开始。

列表式一个有序的可重复元素序列。列表是**可变**的，列表中的元素可以重复，可以是**不同的类型**。


**列表非常重要**，他不仅是python开发中最常用的数据结构，同时也是python序列中最具代表性的一个。 当能够理解列表以后，剩下的其他序列学起来就没有那么困难。

### 2.4.1 列表的创建方法

```python
alist = [1,2,3,4,5,6] #列表使用[]表示，每个元素之间用,隔开
print('alist :',alist)
blist = list("hello world!") #列表也可以使用list()函数将其他可迭代的对象转换为列表，比如字符串。字符串的结构我们会在字符串小节里具体介绍
print('blist :',blist)
```

    alist : [1, 2, 3, 4, 5, 6]
    blist : ['h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd', '!']
    

### 2.4.2 访问元素的方法，索引与切片 

python中的序列均有正向索引与反向索引，正向索引从0开始表示序列第一个元素，反向索引从-1开始表示
以alist为例子，我们打印出alist中每个元素对于的正向索引与反向索引。


```python
print('elements: ','   '.join([str(i) for i in alist]))
print('正向索引:  ','   '.join([str(i) for i in range(0,len(alist))]))
print('反向索引:  ','  '.join([str(i) for i in range(-len(alist),0)]))#这里的len函数是用来获取列表长度的，后面会具体介绍
```

    elements:  1   2   3   4   5   6
    正向索引:   0   1   2   3   4   5
    反向索引:   -6  -5  -4  -3  -2  -1
    


```python
#取列表第一个元素的两种方式
print('第一个元素: ',alist[0])
print('第一个元素: ',alist[-6])

#取列表最后一个元素的两种方式
print('最后一个元素: ',alist[-1])
print('最后一个元素: ',alist[5])

#修改第二个元素
alist[1]=0
print(alist)

#删除第二个元素
del alist[1]
print(alist)
```

    第一个元素:  1
    第一个元素:  1
    最后一个元素:  6
    最后一个元素:  6
    [1, 0, 3, 4, 5, 6]
    [1, 3, 4, 5, 6]
