# Azure SS主机 SS服务安装记录

### 服务端：



1. 先安装pip

   ~~~bash
   [root@server ~]# curl "https://bootstrap.pypa.io/get-pip.py" -o "get-pip.py"
   [root@server ~]# python get-pip.py
   ~~~

2. shadowsocks 配置文件: /etc/shadowsocks.json

   ~~~json
   {
   "server":"52.184.97.225",
       "server_port":4389,
       "local_port":1080,
       "password":"ey$#12-+{s23YH-(22wL<?~{}[]2",
       "timeout":600,
       "method":"aes-256-cfb",
       "fast_open":false
   4389}
   
   
   ~~~

  [1](https://blog.51cto.com/zero01/2064660)

https://blog.51cto.com/xvjunjie/2071369

