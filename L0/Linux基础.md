![image](https://github.com/user-attachments/assets/fbba7384-fdb1-4892-ac09-b5d68b4c4b07)### 1.使用ssh远程连接开发机

进入powerShell终端，输入登录命令及密码即可
![image](https://github.com/user-attachments/assets/490657da-1557-4eed-82b8-d67f77caae3f)
![image](https://github.com/user-attachments/assets/4523b3c4-d4d2-48c3-a7af-9be784bd3e55)


### 2.端口映射
使用 ssh 命令进行端口映射，在开发机页面点击自定义服务
![image](https://github.com/user-attachments/assets/850688d7-bf5a-4b6e-ad32-7bfa77ccbbfc)


输入命令
`ssh -p 35267 root@ssh.intern-ai.org.cn -CNg -L 7860:127.0.0.1:7860 -o StrictHostKeyChecking=no`
到本地终端，在本地浏览器打开
`http://localhost:7860`即可
![image](https://github.com/user-attachments/assets/88e98fee-1e50-4de1-aee2-936ff2849339)
