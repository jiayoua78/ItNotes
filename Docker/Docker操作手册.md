## Docker操作手册

1. #### Centos安装(使用`install docker`)

   ~~~bash
   yum -y install docker #通过yum安装docker很简单。
   ~~~

2. 获取镜像

      ```bash
      docker pull centos #从默认(hub.docker.com)docker仓库拉取名称为centos的镜像。
      docker pull centos:7.6 #拉取名称为centos,标签为7.6的镜像。
      ```

      亦可以在http://hub.docker.com上查看在线镜像仓库列表。注册后可以获得私有在线仓库，允许把自定的镜像push上去。

3. 查看本地镜像

      ```bash
      docker images
      ```

4. 删除本地镜像使用 `rmi` 命令
      ```bash
      docker rmi '镜像ID'
      ```

5. 通过镜像运行容器
      ```bash
      docker run -t -i centos #根据名称为centos的镜像创建一个容器（自动分配一个容器名称），并且进入容器的终端。
      docker run -d -t -i centos #在后台运行容器（自动分配一个容器名称）。
      docker run --name centos1 -it centos #运行一个自定义名称为“centos1”的容器。并且进入容器的终端。
      ```
      说明：选项 `-d` 表明通过后台运行容器。`centos` 容器名称，也可以替换为容器ID。

6. 查看容器列表
      ```bash
      docker ps 
      docker ps -a #包括已经停止的容器
      ```

7. 运行，停止容器（通过`docker ps -a`查看已存在的容器）

        ```bash
        docker start MyCentos1 #启动名称为MyCentos1的容器
        docker stop MyCentos1 #停止名称为MyCentos1的容器
        docker start d160b7faa5bf #启动ID为d160b7faa5bf的容器
        ```

8. 进入正在运行的容器或执行容器中的程序。

   ```bash
   docker exec -it c9e2e318deb6 /bin/bash # 以打开bash的方式进入到ID为c9e2e318deb6的容器,执行此命令之前必须确保此容器正在运行。此命令亦可解释为执行容器中的bash程序。
   ```

9. 以单一进程的方式进入容器（不常用）

   ```bash
   docker attach c9e2e318deb6  #进入ID为c9e2e318deb6的容器，如果以此方式再打开一个终端，实际上他们运行在容器的同一个进程上。若一个终端退出，别的终端也会退出。退出时会停止容器运行
   ```

   

10. 删除容器

   ```bash
   dock rm MyCentos1 #删除名称为MyCentos1的容器。
   dock rm d160b7faa5bf # 删除ID为d160b7faa5bf的容器。
   ```

11. 重命名容器：

     ```bash
     docker rename 原容器名  新容器名
     ```

     

12. 备份容器(容器快照)：

     ```bash
     docker commit -p  d160b7faa5bf ssr-backup1 #提交成为容器快照
     docker images #可以看到刚才提交的容器镜像
     docker login #登入线上镜像仓库（docker hub)
     docker tag '镜像ID' jiayoua/ssr-backup1:1.00 #为镜像贴上标签
     docker push jiayoua/ssr-backup1 #把容器推到线上仓库。
     
     ```
       备份容器相当一制作一个基于这个容器的镜像，然后上载到“hub.docker.com”的镜像仓库，要用的时候再pull下来。 





