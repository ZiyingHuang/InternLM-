## 1.星号 (*) 在变量前
### 1.1“打包”
#### 1.1.1作为函数参数
当在函数参数中使用单个星号时，它表示将多个参数作为**元组**传递给函数。
```python
def foo(*args):
    print(args)

foo(1, 2, 3)  # 输出: (1, 2, 3)
```
#### 1.1.2 赋值操作
在赋值操作中，星号表示“解包”操作，将一个可迭代对象的剩余部分赋值给变量。
```python
# 赋值操作中的解包
a, *b, c = [1, 2, 3, 4, 5]
print(a)  # 输出: 1
print(b)  # 输出: [2, 3, 4]
print(c)  # 输出: 5
```

### 1.2 解包
#### 1.2.1 将列表或元组传递给函数
在调用函数时，星号可以用于将列表或元组解包为函数的多个参数。
```python
def add(x, y):
    return x + y

numbers = [1, 2]
result = add(*numbers)  # 相当于 add(1, 2)
print(result)  # 输出: 3
```
#### 1.2.2 解包字典
双星号 (**) 可以用于解包字典，将字典的键值对作为函数的关键字参数传递。
```python
def greet(name, age):
    print(f"Hello, my name is {name} and I am {age} years old.")

person = {"name": "Alice", "age": 30}
greet(**person)  # 相当于 greet(name="Alice", age=30)
```
