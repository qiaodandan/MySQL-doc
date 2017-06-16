## 安装git
使用下面的命令进行安装git工具.

    $ sudo apt-get install git
    
## 创建版本库

* 第一步, 先要创建一个目录, 这个目录就是用来存放仓库的.

  $ mkdir github
  
  $ ls
  
  $ mkdir demo
  
  $ cd demo/
  
* 第二步, 使用git init命令, 将当前目录创建成git仓库.

  $ git init
  $ ls -al(回车，会发现有一个隐藏的.git目录. 这个目录就是存放着git管理工具用到的所有信息和基本配置信息. 没事千万不要手动修改这个目录, 不然改乱了, git仓库就给破坏了.)
## 提交
提交就是要把需要git管理的文件保存到仓库里, 这种保存类似前面所讲的一个版本的保存;只有把修改的的状态提供到仓库里, 才方便把仓库中把它取出来.

  1. 增加文件:
     1. 当前目录里没有文件, 那么我们先创建一个文件README: $ touch README
     2. 编辑这个文件, 写一点东西在里面:$ vim README
     3. 先用查看当前状态的命令, 查看一下现在目录下文件的状态:$ git status
     4. 把文件加到仓库中去, 只有加到仓库中了, 才可能看一下文件的变化:$ git add README
     5. 现在使用查看状态的命令, 看一下是目录下文件的状态:$ git status 
  2. 提交:$ git commit
  3. 配置用户信息
     1. 配置用户邮箱:$ git config --global user.email
     2. 配置用户名:$ git config --global user.name
     3. 配置编辑器:$ git config --global core.editor vim
## 查看提交信息
  $ git log

