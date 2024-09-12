### 1.随机数np.random
`np.random.rand`与`np.random.random`的区别：  
np.random.rand 允许你直接传入维度参数，而 np.random.random 需要传入一个包含形状信息的元组（tuple），例如：
```python
# 使用 np.random.rand 生成 2x3 矩阵
np.random.rand(2, 3)

# 使用 np.random.random 生成 2x3 矩阵
np.random.random((2, 3))
```
两者在生成随机数方面本质上是相同的，区别在于参数的传递方式。


### 2. numpy生成矩阵
| 方法                     | 功能描述                          | 示例代码                                                         |
|--------------------------|-----------------------------------|------------------------------------------------------------------|
| `np.array()`              | 手动定义矩阵（二维数组）           | `matrix = np.array([[1, 2, 3], [4, 5, 6]])`                      |
| `np.zeros()`              | 生成全零矩阵                      | `zero_matrix = np.zeros((3, 3))`                                 |
| `np.ones()`               | 生成全一矩阵                      | `ones_matrix = np.ones((2, 4))`                                  |
| `np.eye()` 或 `np.identity()` | 生成单位矩阵（对角线为 1）        | `identity_matrix = np.eye(3)`                                    |
| `np.random.rand()`        | 生成随机浮点数矩阵                 | `random_matrix = np.random.rand(3, 3)`                           |
| `np.random.randint()`     | 生成随机整数矩阵                  | `random_int_matrix = np.random.randint(0, 10, (3, 3))`           |
| `np.diag()`               | 生成对角矩阵                      | `diag_matrix = np.diag([1, 2, 3])`                               |
| `np.arange().reshape()`   | 生成等差数列矩阵                  | `arange_matrix = np.arange(1, 10).reshape(3, 3)`                 |
