CentOS7 安装Python3

2019年3月9日

14:51

**一****:** **首先从官网下载****Python3.7.2**

​            <https://www.python.org/downloads/>

**二****:**  **安装依赖包：**

 

1. yum -y groupinstall “Development tools”
2. yum -y install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel

1. yum install      libffi-devel -y  

 

**三：解压，安装**

1. cd Python-3.7.2
2. ./configure –prefix=/usr/local/python3        *#**指定安装目录为**/usr/local/python3*
3. make && make install

 

**四，设置软连接**

1:重命名/usr/bin/ 下面的 pyhton 文件夹为python.bak

\# mv python python.bak

2:执行命令：

 \# ln -s /usr/local/python3/bin/python3 /usr/bin/python

 \# ln -s /usr/local/python3/bin/pip3 /usr/bin/pip3

 

**五：** **设置****yum****指向****python2.7**

 

yum需要python2版本，所以我们还要修改yum的配置，执行：

 

1:vim  /usr/bin/yum

把 #! /usr/bin/python修改为  #! /usr/bin/python2

同理，也要修改修改 /usr/libexec/urlgrabber-ext-down 文件

2:  vim  /usr/libexec/urlgrabber-ext-down

\#! /usr/bin/python 修改为 #! /usr/bin/python2

这样python3版本就安装完成；同时python2也存在