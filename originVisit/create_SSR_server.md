## 创建一个SSR服务器

1. ### 安装

直接参考这个网站教程：[点击这里](https://blog.csdn.net/junmoxi/article/details/80285767)

或者在linux机器上直接运行一下命令就能完成安装：

安装服务器使用的脚本命令行：
```bash
*# 安装wget，如果有则忽略这一步* 

yum -y install wget

*# 下载并安装脚本* 

wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssr.sh && chmod +x ssr.sh && bash ssr.sh
```

2. ### 服务端命令行

   ```bash
   service ssr start #开启ssr服务
   ```

   