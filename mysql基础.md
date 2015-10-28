## 登陆Mysql

```
mysql -h 主机名 -u 用户名 -p
```

## 建库

```
create database samp_db character set utf8;
```

## 使用数据库

```
use 数据库名
```

## 建表

```
create table 表名称(列声明);
```
例子

```
create table students
	（
		id int unsigned not null auto_increment primary key,
		name char(8) not null,
		sex char(4) not null,
		age tinyint unsigned not null,
		tel char(13) null default "-"
	);
```

### 插入数据

```
insert [into] 表名 [(列名1, 列名2, 列名3, ...)] values (值1, 值2, 值3, ...);
```
例子

## 查询数据

```
select 列名称 from 表名称 [查询条件];
```
例子

```
select name, age from students;
```

## 更新

```
update 表名称 set 列名称=新值 where 更新条件;
```

例子

```
update students set tel=default where id=5;
```

## 删除数据

```
delete from 表名称 where 删除条件;
```

例子

```
delete from students where id=2;
```

## 修改表

### 插入字段

```
alter table 表名 add 列名 列数据类型 [after 插入位置];
```

例子

```
alter table students add address char(60);
```

### 删除咧

```
alter table 表名 drop 列名称;
```

例子

```
alter table students drop birthday;
```

### 重命名

```
alter table 表名 rename 新表名;
```

例子

```
alter table students rename workmates;
```

### 删除整张表

```
drop table 表名;
```

例子

```
drop table workmates;
```

### 删除整个数据库

```
drop database 数据库名;
```


例子 


```
drop database samp_db;
```
