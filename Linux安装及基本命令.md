## Linux简介
在1991年，林纳斯·托瓦兹开始在MINIX上开发Linux内核，为MINIX写的软件也可以在Linux内核上使用。后来使用GNU软件代替MINIX的软件，因为使用从GNU系统来的源代码可以自由使用，这对Linux的发展是有益。使用GNU GPL协议的源代码可以被其他项目所使用，只要这些项目使用同样的协议发布。为了让Linux可以在商业上使用，林纳斯·托瓦兹决定更改他原来的协议（这个协议会限制商业使用），以GNU GPL协议来代替。之后许多开发者致力融合GNU元素到Linux中，做出一个有完整功能的、自由的操作系统。

Linux的第一个版本在1991年9月被大学FTP server管理员Ari Lemmke发布在Internet上，最初Torvalds称这个内核的名称为“Freax”，意思是自由（“free”）和奇异（“freak”）的结合字，并且附上“X”这个常用的字母，以配合所谓的类Unix的系统。但是FTP服务器管理员嫌原来的命名“Freax”的名称不好听，把内核的称呼改成“Linux”，当时仅有10000行程序码，仍必须运行于Minix操作系统之上，并且必须使用硬盘开机；随后在10月份第二个版本（0.02版）发布，同时这位芬兰赫尔辛基的大学生在comp.os.minix上发布一则消息

Hello everybody out there using minix- I’m doing a (free) operation system (just a hobby, won’t be big and professional like gnu) for 386(486) AT clones.

1994年3月，Linux1.0版正式发布，Marc Ewing成立Red Hat软件公司，成为最著名的Linux经销商之一。
## Linux 操作系统组成
一个典型的Linux操作系统组成为：Linux内核，一些GNU程序库和工具，命令行shell，图形界面的X Window系统和相应的桌面环境，如KDE或GNOME，并包含数千种从办公套件，编译器，文本编辑器到科学工具的应用软件。

### shell 解释器的介绍
Shell俗称壳（用来区别于核），是指“提供使用者使用界面”的软件（命令解析器）。它类似于DOS下的command和后来的cmd.exe。它接收用户命令，然后调用相应的应用程序，并根据用户输入的指令来反馈给用户指定的信息。

#### shell命令
ls cd mkdir.....

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
