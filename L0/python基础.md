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
