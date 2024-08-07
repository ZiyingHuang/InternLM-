### 1.使用ssh远程连接开发机

进入powerShell终端，输入登录命令及密码即可
![image](https://github.com/user-attachments/assets/490657da-1557-4eed-82b8-d67f77caae3f)
![image](https://github.com/user-attachments/assets/4523b3c4-d4d2-48c3-a7af-9be784bd3e55)


### 2.端口映射
使用 ssh 命令进行端口映射，在开发机页面点击自定义服务
![image](https://github.com/user-attachments/assets/850688d7-bf5a-4b6e-ad32-7bfa77ccbbfc)


输入命令
```
ssh -p 35267 root@ssh.intern-ai.org.cn -CNg -L 8895:127.0.0.1:8895 -o StrictHostKeyChecking=no
```
到本地终端，在本地浏览器打开
`http://localhost:7860`即可（先运行hello_world.py，再进行终端映射）
![image](https://github.com/user-attachments/assets/88e98fee-1e50-4de1-aee2-936ff2849339)


创建一个hello_world.py文件，在文件中填入以下内容：
```
import socket
import re
import gradio as gr
 
# 获取主机名
def get_hostname():
    hostname = socket.gethostname()
    match = re.search(r'-(\d+)$', hostname)
    name = match.group(1)
    
    return name
 
# 创建 Gradio 界面
with gr.Blocks(gr.themes.Soft()) as demo:
    html_code = f"""
            <p align="center">
            <a href="https://intern-ai.org.cn/home">
                <img src="https://intern-ai.org.cn/assets/headerLogo-4ea34f23.svg" alt="Logo" width="20%" style="border-radius: 5px;">
            </a>
            </p>
            <h1 style="text-align: center;">☁️ Welcome {get_hostname()} user, welcome to the ShuSheng LLM Practical Camp Course!</h1>
            <h2 style="text-align: center;">😀 Let’s go on a journey through ShuSheng Island together.</h2>
            <p align="center">
                <a href="https://github.com/InternLM/Tutorial/blob/camp3">
                    <img src="https://oss.lingkongstudy.com.cn/blog/202406301604074.jpg" alt="Logo" width="20%" style="border-radius: 5px;">
                </a>
            </p>

            """
    gr.Markdown(html_code)

demo.launch()
```
在运行代码之前，需要先使用`pip install gradio==4.29.0`命令安装依赖包，然后在终端中运行`hello_world.py`（先运行hello_world.py，再进行终端映射）
![image](https://github.com/user-attachments/assets/0dc4464b-fb8e-4c70-b83d-cec1629c07f3)

本地终端输入映射命令
![image](https://github.com/user-attachments/assets/fa36affc-baf5-467b-a2ff-411c925e817d)
这样就代表成功了。（注意：这个命令不返回任何的内容，这样代表端口映射在运行了，然后在网页中打开连接就可以看到web ui的界面了）
![image](https://github.com/user-attachments/assets/b1dfd856-0403-46e0-90c5-e51c8823a894)


linux详细命令参考连接https://github.com/InternLM/Tutorial/blob/camp3/docs/L0/Linux/readme.md

