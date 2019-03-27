## Git 操作手册

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

3. 如果创建或者修改了文件，需要首先加入到git的暂存区：

   ```bash
   git add .   #提交文件夹内所有文件
   #或者
   git add "文件名称"
   ```


4. 提交到版本库进行管理，创建版本索引

   ```bash
   git commit -m "在这里写上每次提交的注释，以便以后区别"
   ```

   