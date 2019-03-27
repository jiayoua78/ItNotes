## Docker操作手册

1. #### Centos安装(使用`install docker`)

   ~~~bash
   yum -y install docker
   ~~~
2. 获取镜像

      ```bash
      docker pull
      ```
3. 查看本地镜像

      ```bash
      docker images
      ```

4. 通过镜像构建容器
      ```bash
      docker run -t -i centos #或者
      docker run -d -t -i centos
      ```
    说明：选项 `-d` 表明通过后台运行容器。`centos` 容器名称，也可以替换为容器ID。
5. 查看正在运行的容器
      





