# MySQL 关系型数据库
## MySQL安装
### 更新源
用vim打开源列表文件。
```shell
$ sudo vim /etc/apt/sources.list
```
将下面的源粘贴到源列表里。
```shell
deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
##测试版源
deb http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
# 源码
deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
##测试版源
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
# Canonical 合作伙伴和附加
deb http://archive.canonical.com/ubuntu/ xenial partner
deb http://extras.ubuntu.com/ubuntu/ xenial main
```
### Apache安装
```shell
$ sudo apt-get update
$ sudo apt-get install tasksel
$ sudo tasksel
```
选择LAMP sever 空格选中，选中状态有*号->Tab键->【OK】回车
## MySQL 命令行操作
### 连接到本机上的MYSQL。
键入命令mysql -u root -p，回车后提示你输密码.注意用户名前可以有空格也可以没有空格，
但是密码前必须没有空格，否则让你重新输入密码。如果刚安装好MYSQL，超级用户root是没有密码的，
故直接回车即可进入到MYSQL中了，MYSQL的提示符是： mysql>

```shell
$ mysql -u root -p
$ 123456
```
### 连接到远程主机上的MYSQL
假设远程主机的IP为：110.110.110.110，用户名为root,密码为abcd123。则键入以下命令： 
```shell
$ mysql -h110.110.110.110 -u root -p 123;
```
### 退出MYSQL命令： quit（回车）
### 创建数据库
```sql
mysql> create database <数据库名>;
```
### 显示数据库
```sql
mysql> show databases;
```
### 删除数据库
```sql
mysql> drop database <数据库名>;
```
### 使用数据库
```sql
mysql> use <数据库名>;
```
### 创建数据表
```sql
mysql> create table <表名> ( <字段名1> <类型1> [,..<字段名n> <类型n>]);
```
### 删除表
```sql
mysql> drop table <表名>;
```
### 表插入数据
```sql
mysql> insert into <表名> [( <字段名1>[,..<字段名n > ])] values ( 值1 )[, ( 值n )];
```
### 查询表中的数据
```sql
mysql> select <字段1，字段2，...> from < 表名 > where < 表达式 >
```
### 修改表中数据
```sql
mysql> update 表名 set 字段=新值,... where 条件 
```
### 增加字段
```sql
mysql> alter table 表名 add字段 类型 
```
### 删除字段
```sql
mysql> ALTER TABLE table_name DROP field_name;
```













