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


## 任务二
请使用本地vscode连接远程开发机，将上面你写的wordcount函数在开发机上进行debug，体验debug的全流程，并完成一份debug笔记(需要截图)。


### 1.启动debugpy
通过ssh远程连接开发机，配置好`python debugger:Remote Attach`，通过命名好的pyd指令进入debug
![image](https://github.com/user-attachments/assets/873dfe78-d585-41e1-a275-4f33f3aeb640)


### 2.进入第一个断点
此时第一个断点未执行，可以看到左边text变量为原始值
![image](https://github.com/user-attachments/assets/8513a83a-cd4b-44de-b145-6e93846d8d0a)
