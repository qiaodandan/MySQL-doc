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

   
