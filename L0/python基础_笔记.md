### 2.4.4 列表函数与方法

`list.append(obj)`，在列表末尾添加新元素，不返回值
```python
alist = [0,1,1,2,3,4,5,6,7,8]
alist.append(10)#.append不会返回任何内容，直接在原列表上操作
```
    [0, 1, 1, 2, 3, 4, 5, 6, 7, 8, 10]
    
```python
alist.extend([11,12])#.extend不会返回任何内容，直接在原列表上操作
```
    [0, 1, 1, 2, 3, 4, 5, 6, 7, 8, 10, 11, 12]

```python
alist.reverse()#逆向排列列表中的所有元素
alist.sort()#默认将列表中的所有元素按升序排列，没有返回值
alist.sort(reverse=True)#降序
```


copy和clear我们放到一起讲  
如何备份一个alist?直接=和使用copy的区别：alist_copy = alist时并没有新建一个对象，而只是单纯赋值了alist的地址给alist_copy。这会导致我们对变量alist_copy的所有操作本质上都是在操作alist。而当我们使用.copy()方法进行赋值时，会复制alist为一个新的对象，此时对新对象的修改不会影响到alist。

```python
alist = [10, 8, 7, 6, 5, 3, 2, 1, 1, 0, 0]
blist = [10, 8, 7, 6, 5, 3, 2, 1, 1, 0, 0]
alist_copy = alist
blist_copy = blist.copy()

alist_copy.clear()#清空alist_copy
blist_copy.clear()#清空blist_copy

print('alist_copy: ',alist_copy)
print('alist: ',alist)
print('blist_copy: ',blist_copy)
print('blist: ',blist)
```
    alist_copy:  []
    alist:  []
    blist_copy:  []
    blist:  [10, 8, 7, 6, 5, 3, 2, 1, 1, 0, 0]



### 2.6集合
```python
#新建一个集合
aset = {1,2,3,4,5}
#新建一个空集合
aset = set()
print('这是一个空集合: ',aset)
```
    这是一个空集合:  set()

```python
#将其他序列转换成集合,注意观察转换前后的变化
alist = [1,1,1,1,2,2,2,2,3,3,3]
print('alist: ',alist)
aset = set(alist)
print('aset: ',aset)
```
    alist:  [1, 1, 1, 1, 2, 2, 2, 2, 3, 3, 3]
    aset:  {1, 2, 3}
