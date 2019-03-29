# Linux 操作手册

1. 本地文件上载到服务器：

   ```bash
   scp /path/filename username@servername:/path 
   # 例如：
   scp ./1.txt milo@xxx.xxx.xxx.xxx:/home/milo/
   ```

2. 从服务器下载:

   ```bash
   scp username@servername:/path/filename /var/www/local_dir
   ```

   

   3、从服务器下载整个目录
   scp -r username@servername:/var/www/remote_dir/（远程目录） /var/www/local_dir（本地目录）

   例如:scp -r root@192.168.0.101:/var/www/test  /var/www/  

   4、上传目录到服务器
   scp  -r local_dir username@servername:remote_dir
   例如：scp -r test  root@192.168.0.101:/var/www/   把当前目录下的test目录上传到服务器的/var/www/ 目录

3. Ubuntu 修改时区

   ~~~bash
   #所有的时区名称存储在/usr/share/zoneinfo文件中。
   timedatectl set-timezone "Asia/Shanghai" #执行此命令就可以将时区设为上海时区。
   timedatectl status #查看时区状态
   #或者
   date #查看时区状态
   ~~~

   
