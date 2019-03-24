# Git Commands

#### 取消某文件夹的git管理.

~~~bash
find . -name ".git" | xargs rm -Rf
~~~

一、使用git rm 命令

1.预览要删除的文件

执行 git rm -r -n --cached "bin/"   ，此命令是展示要删除的文件表预览

2.移除版本控制操作

```bash
执行 git rm -r --cached  "bin/"    # 删除文件的命令. 
执行 git commit -m" 删除bin文件"    # 提交，并加注释
执行 git push origin master   　　  # 提交到远程服务器
```

注：此删除保留本地文件，如果删除服务器文件可以不使用推送。


当我们需要删除暂存区或分支上的文件, 同时工作区也不需要这个文件了, 可以使用

1 git rm file_path
2 git commit -m 'delete somefile'
3 git push

当我们需要删除暂存区或分支上的文件, 但本地又需要使用, 只是不希望这个文件被版本控制, 可以使用

git rm --cached file_path
git commit -m 'delete remote somefile



## 目录结构如下

```bash
project
    bin
    lib
    src
    ...... 
```

## 执行如下的操作

```bash
git add .
git commit -m "add bin/ lib/ src/"
git push origin master
```

 

突然发现原来 `lib` 目录不需要提交到版本库,但是现在远程已经存在该目录,what should I do.（吐出去的东西还能收回来吗）

万能的[Git](http://lib.csdn.net/base/git)啊,help me！

功夫不负有心人,找到了解决问题的方法,其实就是 `git rm` 的命令行参数。

## `git rm` 命令参数

```
-n --dry-run 
Don’t actually remove any file(s). Instead, just show if they exist in the index and would otherwise be removed by the command.
-r 
Allow recursive removal when a leading directory name is given. 
--cached 
Use this option to unstage and remove paths only from the index. Working tree files, whether modified or not, will be left alone.
```

## 解决方法

```
git rm -r -n --cached "bin/" //-n：加上这个参数，执行命令时，是不会删除任何文件，而是展示此命令要删除的文件列表预览。
git rm -r --cached  "bin/"      //最终执行命令. 
git commit -m" remove bin folder all file out of control"    //提交
git push origin master   //提交到远程服务器
```

此时 `git status` 看到 bin/目录状态变为 `untracked`

可以修改 `.gitignore` 文件 添加 `bin/` 并提交 `.gitignore` 文件到远程服务器,这样就可以不对bin目录进行版本管理了。

以后需要的时候,只需要注释 `.gitignore` 里 `#bin/` 内容,重新执行 `git bin/` ,即可重新纳入版本管理。