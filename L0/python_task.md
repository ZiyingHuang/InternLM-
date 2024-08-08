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


### 2.开始debug
进入第一个断点。

此时第一个断点未执行，可以看到左边text变量为原始值
![image](https://github.com/user-attachments/assets/8513a83a-cd4b-44de-b145-6e93846d8d0a)



执行完第一个断点并进入第二个断点，可以看到此时原字符串已经转换为小写字母，word_count字典也开始根据单词出现次数来统计
![image](https://github.com/user-attachments/assets/5fe5e126-2eb5-410b-8c4d-ada251a5a973)



再进入下一个断点，可以看到此时已经执行完上一断点的语句，将非字母的符号转换为空格
![image](https://github.com/user-attachments/assets/658075f6-5082-426c-8c49-741d03c47989)



进入下一断点，此时已经用.split()函数将字符串分割成单词并存入words列表中，.split()函数可以自动去除连续的空白字符
![image](https://github.com/user-attachments/assets/dcda30fa-c082-4990-a982-d0ba10d5edc3)



最后正确输出结果
![image](https://github.com/user-attachments/assets/0b3cb318-7c0b-496e-98f2-3023843f83b1)
