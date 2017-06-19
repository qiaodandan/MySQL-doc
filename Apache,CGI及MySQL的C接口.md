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
git status
make install
git status
```













   
