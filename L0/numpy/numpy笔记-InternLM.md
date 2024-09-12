## 3.1 numpy Ndarry和创建数组的方式
NumPy数组（ndarray）是NumPy库的核心数据结构，它是一系列同类型数据的集合，以 0 下标为开始进行集合中元素的索引。  

ndarray本质上是一个存放**同类型元素**的多维数组，其中的每个元素在内存中都有相同存储大小的区域。  

NumPy数组（ndarray）的特点：

1. 高效的内存使用：ndarray对象在内存中连续存储，这使得对数组的元素进行切片和迭代等操作非常快速，而不需要额外的内存开销。

2. 快速执行：NumPy数组的操作是在编译后的代码中执行的，这使得NumPy操作比纯Python代码快得多。
   
3. 方便易用：NumPy提供了大量数学和数值计算函数，使得数组操作非常方便。
   
4. 灵活性：NumPy数组可以在不同的数据类型之间灵活转换，支持整数、浮点数、复数等多种数据类型。


创建numpy数组最常见的方法就是将一个列表使用np.array()函数转成ndarray。
TIPS:在notebook中将光标移动到函数的括号中间，按下shift+tab可以看到函数的提示
```python
import numpy as np
array1 = np.array([1,2,3,4,5])
#np.array函数全部的参数有
#np.array(object, dtype=None, *, copy=True, order='K', subok=False, ndmin=0,like=None)
#具体可以尝试上面提到的查看函数提示的方法或者去看numpy的文档
#dtype参数表示array中元素的类型，这个参数在numpy中很常见。
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
