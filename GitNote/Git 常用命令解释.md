## Git 常用命令解释

1. 初始化git管理的文件夹：

   进入到文件夹，鼠标右键，选择"Git Here",然受输入

   ~~~bash
   git init
   ~~~

   git 会在此文件夹当中建立一个隐藏的.git文件夹。

2. 登记用户：

   如果初次使用，需要先登记用户：

   ```bash
   git config --global user.name "your name"
   git config --global user.email "your email"
   ```

3. 如果创建或者修改了文件，需要首先提交到git的暂存区：

   ```bash
   git add .   #提交文件夹内所有文件
   #或者
   git add "文件名称"
   ```

   