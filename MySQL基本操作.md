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
