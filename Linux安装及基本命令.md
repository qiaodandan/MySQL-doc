## Linux 操作系统组成
一个典型的Linux操作系统组成为：Linux内核，一些GNU程序库和工具，命令行shell，图形界面的X Window系统和相应的桌面环境，如KDE或GNOME，并包含数千种从办公套件，编译器，文本编辑器到科学工具的应用软件。
![linux组成](https://raw.githubusercontent.com/qiaodandan/MySQL-doc/master/linux组成.jpg)
### shell 解释器的介绍
Shell俗称壳（用来区别于核），是指“提供使用者使用界面”的软件（命令解析器）。它类似于DOS下的command和后来的cmd.exe。它接收用户命令，然后调用相应的应用程序，并根据用户输入的指令来反馈给用户指定的信息。

#### shell命令(老师讲过的，不全)
* C

cat xxx 浏览文件xxx的内容

cat xxx1 xxx2 浏览多个文件的内容

cd 回到起始目录，也即刚登陆到系统的目录，cd后面无参数

cd / 回到根目录

cd .. 返回上一级目录

cd - 返回到最近使用的目录

* L

ls -al 列出所有文件的完整信息，每行一个文件

ls 列出所有文件

* P

pwd 显示当前目录

ps 列出当前用户的进程

ps -ef 以完整信息列出所有进程

* R

rm -rf xxx 删除目录xxx及其子目录，即使目录不空

rm -rf xxx/* 删除目录xxx下的所有内容，但不删除xxx本身

rm -rf * 删除当前目录下所有文件，包括子文件加及其中的文件，-r表示递归，-f表示强制删除，不询问。

rmdir xxx 删除空目录xxx

mkdir xxx 创建目录xxx

* T

tar -xvf xxx.tar 将xxx.tar解压，解压后将产生xxx文件夹，里面包含解压后的文件 x表示解压，v表示输出解压信息，f表示操作普通文件

tar -cvf tmp.tar tmp 将文件夹tmp打包成tmp.tar

tar -rvf tmp.tar zzz 将文件zzz追加到tmp.tar中

touch命令

touch abc 如果文件abc存在，则更新其时间为当前时间，否则创建它

* Z

zip 压缩

zip -r9 ~/zdd /home/zdd/* 将目录/home/zdd下的所有文件压缩并放入当前目录下名为zdd。-r表示递归处理文件夹中的文件,9表示最大压缩率。

unzip 解压缩

unzip -d ~/zdd zdd.zip 将zdd.zip解压到当前目录下的zdd目录中，-d表示指定解压目录。

gzip 压缩/解压缩

gzip -d error_log.gz 将error_log.gz解压缩，-d表示解压缩，解压缩后error_log.gz将不复存在。


* 其他

在终端上翻页(Putty窗口也可以)

向上翻页    Shift+PageUp

向下翻页    Shift+PageDown

### 文本编辑器Vim的基本使用
#### Vim介绍
Vim是一个类似于Vi的著名的功能强大、高度可定制的文本编辑器，在Vi的基础上改进和增加了很多特性。Vim是纯粹的自由软件在代码补全、编译及错误跳转等方便编程的功能特别丰富，在程序员中被广泛使用，和Emacs并列成为类Unix系统用户最喜欢的文本编辑器。

#### Vim的基本使用
* i：在当前字符的左边插入
* I：在当前行首插入
* a：在当前字符的右边插入
* A：在当前行尾插入
* o：在当前行下面插入一个新行
* O：在当前行上面插入一个新
* h: 向前移动一个字符
* j: 向上移动一行
* k: 向下移动一行
* l: 向后移动一个字符
* yy: 复制当前一行
* dd:剪切当前一行
* p: 粘贴内容到游标之后
* P: 粘贴内容到游标之前
#### 基本的文件操作
* 文件的创建:touch  file 
* 删除:rm  file
* 复制:cp file file1
* 重命名:mv file   file2
* 列出文件列表:ls -al 
* 查看文件内容:cat  file
#### 基本的目录操作
* 目录的创建:mkdir dir
* 删除:rmdir xxx 删除空目录xxx
* 复制:cp dir   dir1  -a
* 重命名:mv dir  dir2
* 列出目录列表:ls -d  dir
* 目录中查找文件:find  ./dir  -name  "filename"



