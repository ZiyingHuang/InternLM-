## 3.1 numpy Ndarry和创建数组的方式
NumPy数组（ndarray）是NumPy库的核心数据结构，它是一系列同类型数据的集合，以 0 下标为开始进行集合中元素的索引。  

ndarray本质上是一个存放**同类型元素**的多维数组，其中的每个元素在内存中都有相同存储大小的区域。  

创建numpy数组最常见的方法就是将一个列表使用np.array()函数转成ndarray。
TIPS:在notebook中将光标移动到函数的括号中间，按下shift+tab可以看到函数的提示
```python
array1 = np.array([1,2,3,4,5])
print('array1: \n',array1)
array2 = np.array([[1,2],[3,4]])
print('array2: \n ',array2)
```
```
array1: 
 [1 2 3 4 5]
array2: 
  [[1 2]
 [3 4]]
```




### 3.2.5 拼接数组
numpy有四种拼接数组的函数:
1. np.concatenate
* 功能：concatenate 沿着现有的轴将多个数组连接在一起。它不会增加新的维度，只是在现有维度上将数组拼接起来。
* 维度不变：使用 concatenate 后，结果数组的维度与输入数组相同。
* 输入要求：除了拼接的轴之外，**其他轴的大小必须相同**。例如，如果在轴 0 上拼接两个数组，它们的其他维度必须相同。
```python
np.concatenate(arrays, axis=0)
```
* arrays：要拼接的数组列表。
* axis：沿着哪个轴进行拼接，默认为 0。
