##  安装atmo
1. 进入atom.io网站
2. other platform
3. atom-amd64.deb(复制链接地址)
4. wget -c 粘贴链接地址
5. sudo dpkg -i atom-amd64.deb
6. 进入atom->edit->preferences->勾选soft wrap和foft wrap At lihe
7. 进入atom->install->安装Atom editor开环境使用的插件
8. 用atom .来编辑文件
## 下载资料cgi-stu
下载->解压->把stu复制到github下
## Apache安装
```shell
 sudo apt-get update
 sudo apt-get install tasksel
 sudo tasksel
```
## Apache开启CGI
需要在apache中开启cgi支持.
```shell
sudo ln -s /etc/apache2/mods-available/cgi.load /etc/apache2/mods-enabled/cgi.load
```
需要重启 apache 服务器
```shell
service apache2 restart
```
改完目录的权限, 方便对目录下的文件写.
```shell
sudo mkdir /usr/lib/cgi-bin/sx
sudo chmod 777 /usr/lib/cgi-bin/sx
```
## Makefile
```shell
vim Makefile
```
```
install:
	cp *.cgi /usr/lib/cgi-bin/sx
```
## MySQL的C接口介绍
安装mysql的C语言库
```shell
sudo apt-get update
sudo apt-get install libmysqlclient-dev
```
## CCGI 基本使用
### 获取表单数据
```
cgiFormResultType  cgiFormString(char *name, char *result, int max);
参数：  name, 指定要获取的表单项的名字
       result,将获得的数据存储到result中
       max， 指定最多读取的字符个数

比如： cgiFormString("name", result,  16);可以获得最多16个字符并且保存于result中
```
### 补充函数fprintf
```
int fprintf(FILE *stream, const char *format, ...);
功能： 将格式化的语句输出到指定的流
fprintf(stdin, "helloworld\n")  等价于 printf("helloworld\n);
```
### 补充函数atoi
```
int atoi(const char *nptr);
功能：将一个字符串转换成对应的数字，比如：“1234” ==》 1234
```
### 接口介绍
```
手册：mysql Documentation
编写：#include <mysql/mysql.h>
编译：gcc  test.c  -o test  -lmysqlclient

MYSQL *mysql_init(MYSQL *mysql)
功能：初始化函数，参数为NULL即可，接收返回值。
     失败，NULL

MYSQL *mysql_real_connect(MYSQL *mysql, const char *host, const char *user, const char *passwd, const char *db, unsigned int port, const char *unix_socket, unsigned long client_flag)
功能：连接mysql服务器
      失败，NULL

void mysql_close(MYSQL *mysql)
功能：关闭服务器连接

int mysql_real_query(MYSQL *mysql, const char *stmt_str, unsigned long length)
功能：执行sql语句，sql语句不能以“；”结尾
      成功，0
      失败， 非0

int mysql_query(MYSQL *mysql, const char *stmt_str)
功能：执行sql语句，sql语句不能以“；”结尾

MYSQL_RES *mysql_store_result(MYSQL *mysql)
功能：存储 mysql_query()  或者  mysql_read_query() 的数据
     失败， NULL

MYSQL_RES *mysql_use_result(MYSQL *mysql)
功能：接收结果，速度要比mysql_use_result()快。

void mysql_free_result(MYSQL_RES *result)
功能：释放空间

my_ulonglong mysql_num_rows(MYSQL_RES *result)
功能：返回 mysql_store_result 的记录个数

my_ulonglong mysql_affected_rows(MYSQL *mysql)
功能：得到执行sql语句之后改变的记录数

const char *mysql_error(MYSQL *mysql)
功能：返回出错提示

MYSQL_FIELD *mysql_fetch_field(MYSQL_RES *result)
功能：返回集合中列的定义   
MYSQL_FIELD *field;

while((field = mysql_fetch_field(result)))
{
    printf("field name %s\n", field->name);
}

MYSQL_FIELD *mysql_fetch_fields(MYSQL_RES *result)
功能：返回集合中列的数组
unsigned int num_fields;
unsigned int i;
MYSQL_FIELD *fields;

num_fields = mysql_num_fields(result);
fields = mysql_fetch_fields(result);
for(i = 0; i < num_fields; i++)
{
   printf("Field %u is %s\n", i, fields[i].name);
}

unsigned int mysql_num_fields(MYSQL_RES *result)
功能：返回集合中列的个数

my_ulonglong mysql_num_rows(MYSQL_RES *result）
功能：返回集合中行的个数
MYSQL_ROW mysql_fetch_row(MYSQL_RES *result)
功能：返回集合中的一行， 结束或者错误返回NULL

unsigned long *mysql_fetch_lengths(MYSQL_RES *result)
功能：返回当前行中每一个字段值的长度 数组。
```
## Atom editor 开环境使用的插件
* activate-power-mode：动感插件 atl + ctrl + o :打开插件
* vim-mode：vim模式
* ex-mode：实现:w功能
* monokai：高亮显示
* atom-ternjs：JavaScript 自动补全
* autoprefixer：给 CSS 添加适当的前缀
* color-picker：选颜色
* emmet：写 HTML 的神器
* atom-beautify：美化代码，空格啊什么什么的
* autoclose-html：HTML自动补全闭标签
* file-icons: 增加许多图标,在侧边蓝文件名前面的icon,,很赞
* autocomplete-modules: 自动补全插件, 有HTML, CSS, python 等
* highlight-selected: 高亮当前所选的文字, 双击后全文这个词或变量都会变高亮.
* Open In Browser: 右键打开浏览器.
* atom-clock: 在bar显示 时间
* autocomplete-js-import: 模块导入智能提示
* autocomplete-modules: 模块智能提示【node_modules】
## MVC
M是指业务模型，V是指用户界面，C则是控制器
* Model（模型）表示应用程序核心（比如数据库记录列表）。
* View（视图）显示数据（数据库记录）。
* Controller（控制器）处理输入（写入数据库记录）。
在stu目录下
```shell
cp -r public/ index.html /var/www/html/
```
改完程序
```shell
make clean
make 
make install
```













   
