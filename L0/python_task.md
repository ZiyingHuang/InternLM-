## 任务一
请实现一个wordcount函数，统计英文字符串中每个单词出现的次数。返回一个字典，key为单词，value为对应单词出现的次数。

```python
def wordcount(text):
    # 将字符串转换为小写
    text = text.lower()
    
    # 创建一个新的字符串，其中非字母字符被替换为空格
    cleaned_text = ''.join(char if char.isalpha() else ' ' for char in text)
    
    # 使用split方法将字符串分割成单词列表
    words = cleaned_text.split()
    
    # 创建一个空字典用于存储单词计数
    word_count = {}
    
    # 遍历单词列表，统计每个单词的出现次数
    for word in words:
        if word in word_count:
            word_count[word] += 1
        else:
            word_count[word] = 1
            
    return word_count

# 测试
text = '''Hello!!  world!  
This is an example.  
Word count is fun.  
Is it fun to count words?  
Yes, it is fun!'''

print(wordcount(text))
```


Output:
```
{'hello': 1, 'world': 1, 'this': 1, 'is': 4, 'an': 1, 'example': 1, 'word': 1, 'count': 2, 'fun': 3, 'it': 2, 'to': 1, 'words': 1, 'yes': 1}
```
![image](https://github.com/user-attachments/assets/332b5d7d-2c0f-413c-befa-5724b5703837)
