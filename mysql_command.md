## 登录

```
mysql -u <user_name> -p <passwd>
```
## 退出

```
exit
```

# 数据库操作

## 查看数据库

```
show databases;
```

## 创建数据库

```
create database <database_name> [operations];
```

## 选择数据库

```
use <database_name>;
```

## 删除数据库

```
drop database <database_name>;
```

# 表操作

## 查看数据库中有哪些表

```
show tables;
```

## 查看表样式

```
describe <table_name>;
```

## 创建表

```
create table <table_name>(<columns>)

e.g.
create table students
	（
		id int unsigned not null auto_increment primary key,
		name char(8) not null,
		sex char(4) not null,
		age tinyint unsigned not null,
		tel char(13) null default "-"
	);
```

## 删除整张表

```
drop table <table_name>;
```

## 向表中插入数据

```
insert [into] <table_name> [(column1, column2, ...)] values (value1, value2, ...);

e.g.
insert into students (name, sex, age) values("孙丽华", "女", 21);
```

## 查询表中的数据

```
select <column1, column2, ...> from <table_name> [conditions];

e.g.
select name, age from students;
```

## 更新表中数据

```
update <table_name> set <column>=<new_value> [conditions];

e.g.
update students set age=age+1;
update students set name="张伟鹏", age=19 where tel="13288097888"; 
```

## 删除表中数据

```
delete from <table_name> [conditions];
```

## 添加列

```
alter table <table_name> add <column1> <data_type> [after <column2>];

e.g.
alter table students add birthday date after age;
```

## 修改列

```
alter table <table_name> change <column_old> <column_new> <data_type_new>

e.g.
alter table students change tel telphone char(13) default "-";
```

## 删除列

```
alter table <table_name> drop <column>;

e.g.
alter table students drop birthday;
```

## 重命名表

```
alter table <table_name_old> rename <table_name_new>;

e.g.
alter table students rename workmates;
```


