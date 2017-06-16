## Linux 操作系统组成
一个典型的Linux操作系统组成为：Linux内核，一些GNU程序库和工具，命令行shell，图形界面的X Window系统和相应的桌面环境，如KDE或GNOME，并包含数千种从办公套件，编译器，文本编辑器到科学工具的应用软件。

### shell 解释器的介绍
Shell俗称壳（用来区别于核），是指“提供使用者使用界面”的软件（命令解析器）。它类似于DOS下的command和后来的cmd.exe。它接收用户命令，然后调用相应的应用程序，并根据用户输入的指令来反馈给用户指定的信息。

#### shell命令
* C

cat xxx 浏览文件xxx的内容

cat xxx1 xxx2 浏览多个文件的内容

cd 回到起始目录，也即刚登陆到系统的目录，cd后面无参数

cd / 回到根目录

cd .. 返回上一级目录

cd - 返回到最近使用的目录

D
df -kh 查看磁盘信息

du -sh foldername 查看文件夹大小，-h表示以human readable格式显示大小，-s表示累加各个文件的大小。

H
history 显示命令历史记录
hostname 显示当前登录的主机名

L

ls -al 列出所有文件的完整信息，每行一个文件

ls -tl 按最后修改时间排序

ls -ul 按最后访问时间排序

ls -R 递归现实子目录中的文件及文件夹，这个命令配合grep可以方便的实现查找，比如在当前目录及子目录下查找文件zdd，ls -R | grep zdd

ls -F | grep / 只列出目录

less 分屏显示文件，按空格向下查看，并可使用上下箭头前后回看。按q键退出。

M

more 分屏显示文件，按空格向下查看，不支持回看，按q键退出。
man ls 查看ls命令的帮助，如果帮助有多页

空格    向下翻页
b    向上翻页
q    退出帮助

O

od 查看文件的ASCII编码。

P
pwd 显示当前目录
ps 列出当前用户的进程
ps -ef 以完整信息列出所有进程

R
rm -rf zdd 删除目录zdd及其子目录，即使目录不空
rm -rf zdd/* 删除目录zdd下的所有内容，但不删除zdd本身
rm -rf * 删除当前目录下所有文件，包括子文件加及其中的文件，-r表示递归，-f表示强制删除，不询问。
rmdir zdd 删除空目录zdd
mkdir zdd 创建目录zdd

S
set 查看已定义变量
ssh hostname 登录到hostname

T
tar [option] file or dir
tar -xvf zdd.tar 将zdd.tar解压，解压后将产生zdd文件夹，里面包含解压后的文件 x表示解压，v表示输出解压信息，f表示操作普通文件
tar -cvf tmp.tar tmp 将文件夹tmp打包成tmp.tar
tar -rvf tmp.tar zzz 将文件zzz追加到tmp.tar中
touch命令
touch [acm] -t time file
这个命令用来修改文件的时间，a-access time, m-modification time c-do not create if file not exists
如果不指定时间，则使用当前的系统时间，如果文件不存在，且未指定-c那么将创建新的文件。可以使用这个方法快速创建文件。time的格式如下
[[CC]YY]MMDDhhmm[.SS]
touch abc 如果文件abc存在，则更新其时间为当前时间，否则创建它
touch abc -a -t
touch -m -t 201101230621 abc

W
who 查看有哪些人登陆了系统

who am i 查看自己的账户信息

which ls 查看ls程序所在的路径。

Z
zip 压缩
zip [options] dest_files source
zip -r9 ~/zdd /home/zdd/* 将目录/home/zdd下的所有文件压缩并放入当前目录下名为zdd。-r表示递归处理文件夹中的文件,9表示最大压缩率。

unzip 解压缩
unzip -d ~/zdd zdd.zip 将zdd.zip解压到当前目录下的zdd目录中，-d表示指定解压目录。

gzip 压缩/解压缩
gzip -d error_log.gz 将error_log.gz解压缩，-d表示解压缩，解压缩后error_log.gz将不复存在。


其他
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

