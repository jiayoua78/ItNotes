# Git Commands

**Local**

~~~bash
git --help      #  get help
git add .       # 添加全部文件进暂存区
git add XX      #      把xx文件添加到暂存区去。
git init         # 把当前的目录变成可以管理的git仓库，生成隐藏.git文件。		
git branch brancName # create the new branch
git branch  # 查看当前所有的分支
git branch -d dev # 删除dev分支
git branch name # 创建分支
git log   # 查看每次提交的列表，HEAD指针指向哪里
git log --oneline --graph #look over the git log in a simple way,
                          #the option "--graph" help you can check the ranch on graph
find . -name ".git" | xargs rm -Rf    # Cancel  manager the folder(delete the folder of ".git")
git add 文件名 #添加单个文件进暂存区
git status # 查看工作区内文件的状态
git commit -m "说明" # 提交更改（只会提交暂存区内的更改）
git checkout -- XX # 把XX文件在工作区的修改全部撤销(还原还未add的文件)。
git checkout -b dev # 创建dev分支 并切换到dev分支上
git checkout master # 切换回master分支
git rest #重置。
git reset HEAD -- 文件名 #把文件移出暂存区（再用checkout命令可以还原文件)
git reset  --hard HEAD^** ：或者 **git reset  --hard HEAD~**  #  回退到上一个版本(如果想回退到100个版本，使用**git reset --hard HEAD~100** )
git diff  XX     # 查看XX文件修改了那些内容
pwd #打印当前所在目录
cat XX   #      查看XX文件内容
git reflog # 查看历史记录的版本号id
git rm XX    # 删除XX文件
git merge dev # 在当前的分支上合并dev分支
git stash # 把当前的工作隐藏起来 等以后恢复现场后继续工作
git stash list # 查看所有被隐藏的文件列表
git stash apply # 恢复被隐藏的文件，但是内容不删除
git stash drop # 删除文件
git stash pop # 恢复文件的同时 也删除文件
~~~

**Remote**
=======

~~~bash
ssh-keygen -t rsa -C "UserEmail" # 跟据UserEmail创建密匙
git remote  # 查看远程库的信息
git remote -v # 查看远程库的详细信息
git push origin master # Git会把master分支推送到远程库对应的远程分支上
git remote add origin https://github.com/RTplay/testgit.git     # 关联一个远程库
git push -u(第一次要用-u 以后不需要) origin master # 把当前master分支推送到远程库
git clone https://github.com/RTplay/testgit.git # 从远程库中克隆
~~~

