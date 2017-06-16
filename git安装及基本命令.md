## 安装git
 使用下面的命令进行安装git工具.
    ```shell
    $ sudo apt-get install git 
    ```    
### 创建版本库

* 第一步, 先要创建一个目录, 这个目录就是用来存放仓库的.
```shell
  $ mkdir github  
  $ ls  
  $ mkdir demo  
  $ cd demo/
```
* 第二步, 使用git init命令, 将当前目录创建成git仓库.
```shell
  $ git init
  $ ls -al
```
会发现有一个隐藏的.git目录. 这个目录就是存放着git管理工具用到的所有信息和基本配置信息. 没事千万不要手动修改这个目录, 不然改乱了, git仓库就给破坏了.
### 提交
提交就是要把需要git管理的文件保存到仓库里, 这种保存类似前面所讲的一个版本的保存;只有把修改的的状态提供到仓库里, 才方便把仓库中把它取出来.

  1. 增加文件:
     1. 当前目录里没有文件, 那么我们先创建一个文件README: 
     
     ```shell
     $ touch README
     ```
     2. 编辑这个文件, 写一点东西在里面:
     
     ```shell
     $ vim README
     ```
     3. 先用查看当前状态的命令, 查看一下现在目录下文件的状态:
     
     ```shell
     $ git status
     ```
     4. 把文件加到仓库中去, 只有加到仓库中了, 才可能看一下文件的变化:
     
     ```shell
     $ git add README
     ```
     5. 现在使用查看状态的命令, 看一下是目录下文件的状态:
     
     ```shell
     $ git status 
     ```
  2. 提交:
     ```shell
     $ git commit
     ```
  3. 配置用户信息
     1. 配置用户邮箱:
     ```shell
     $ git config --global user.email
     ```
     2. 配置用户名:
     ```shell
     $ git config --global user.name
     ```
     3. 配置编辑器:
     ```shell
     $ git config --global core.editor vim
     ```
### 查看提交信息
    $ git log
## git的基本命令
  ### 删除文件恢复
     1. 把仓库里的README这个文件给删除
     $ rm README
     $ ls
     $ ls -al
     2. 文件已经被删除,查看一下现在仓库是什么状态
     $ git status
     3. 恢复:前提是这个文件提交到了仓库
     $ git checkout README
     4. 然后我们再用ls查看一下文件是否存在.
     $ ls -al
     5. 再查看git仓库是状态
     $ git status
  ### 版本回退
     1. 如果想回退到上次提交的版本, 那么需要使用git reset命令.
     $ git reset --hard commitID
     2. git reset命令恢复到前面提交版本.
     $ git reflog
  ### 从仓库中删除文件
     1. 将文件从仓库中删除这个文件.(这只是做了删除操作, 但没有真正的从仓库中删除)
     $ git rm filename
     2.  我们做一次提交(从仓库删除).
     $ git commit
  ### 从版本库中忽略文件
     $ touch .gitignore
  ### 版本之间对比
  ```shell
  $ git diff
  $ git diff commitID1 commitID2
  ```
  ### git生成patch(patch实际上是保存两个文件的差异.)
  ```shell
  $ git format-patch -p1
  ```
  ### git 打 patch
  ```shell
  $ git am patch-name
  ```
