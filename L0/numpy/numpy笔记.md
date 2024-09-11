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
