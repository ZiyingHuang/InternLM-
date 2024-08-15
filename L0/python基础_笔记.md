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
#### 2.6.1创建集合
```python
#新建一个集合
aset = {1,2,3,4,5}
#新建一个空集合
aset = set()
print('这是一个空集合: ',aset)
```
    这是一个空集合:  set()

#### 2.6.2函数set()：转换成集合
函数set()作用：
* 创建空集合
* 将其他序列转换成集合
  
```python
#将其他序列转换成集合,注意观察转换前后的变化
alist = [1,1,1,1,2,2,2,2,3,3,3]
print('alist: ',alist)
aset = set(alist)
print('aset: ',aset)
```
    alist:  [1, 1, 1, 1, 2, 2, 2, 2, 3, 3, 3]
    aset:  {1, 2, 3}

```python
#合并两个集合
print('aset: ',aset)
print('bset: ',bset)
aset.update(bset)
print('aset.update(bset)后的aset :',aset)
```
    aset:  {1, 2, 3, 4}
    bset:  {3, 4, 5}
    aset.update(bset)后的aset : {1, 2, 3, 4, 5}

### 对比list和set的pop和删除方法
#### 2.6.3 pop
`value = list.pop([index=-1])`  
移除列表中的一个元素（默认最后一个元素），并且返回该元素的值

`value = set.pop()`  
随机移除元素，返回被移除的元素（对比列表是最后一个元素，集合的**随机**可以理解为集合的无序性）

#### 2.6.4 移除操作
`list.remove(obj)`  
移除列表中某个值**第一个**匹配项，不返回值

`set.remove(val)`移除指定元素，不返回值  
`set.discard(val)`删除指定元素，不返回值  
两个作用一样





### 2.8 字符串
#### 2.8.1
##### 2.8.1.1 特殊字符
制表符`\t`：跳到下一个制表位（不是加入四个空格）
换行符`\n`  
（都是反斜杠）

#### 2.8.2
要注意的是，因为字符串是不可修改的对象，所以每个修改字符串的方法都是将修改后的字符串作为一个新对象返回。  
（可以将原对象使用方法后赋值给原对象，按上面的说法此时的“原对象”应该是新对象了，只不过还可以用原来这个名字）

```python
#首先我们把这句话中所有的字母都转换为小写
text = text.lower()
#再用replace把所有的标点符号去掉
text = text.replace(','," ").replace(':'," ").replace('.'," ")
#再用split把这句话拆成词组成的列表
word_list = text.split(" ")
#再用join函数用，把这个列表拼会一个字符串
print(','.join(word_list))
```
    success is not final, failure is not fatal: it is the courage to continue that counts.
    success is not final  failure is not fatal  it is the courage to continue that counts 
    ['success', 'is', 'not', 'final', '', 'failure', 'is', 'not', 'fatal', '', 'it', 'is', 'the', 'courage', 'to', 'continue', 'that', 'counts', '']
    success,is,not,final,,failure,is,not,fatal,,it,is,the,courage,to,continue,that,counts,

注意看上面使用的是`.split(" ")`，当出现连续空格，最后得到的结果会有空字符`''`。如果不想出现这种情况就用`.split()`，括号里不加任何东西，自动将所有连续的空白字符看成是一个来进行分割（空白字符包括空格、换行符`\n`、制表符`\t`）
##### split
    str.split(ch="", num=string.count(str))
以 ch 为分隔符截取字符串，如果 num 有指定值，则仅截取 num+1 个子字符串
