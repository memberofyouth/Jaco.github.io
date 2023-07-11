```
创建数据库 - 指定编码
CREATE DATABASE `dicdb` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;


CREATE DATABASE `integral_platform` DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;



创建用户
CREATE USER strapi IDENTIFIED BY 'strapi123';

创建数据库
CREATE DATABASE `strapi` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;

授权
grant all privileges on strapi.* to 'strapi'@'%';

刷新权限
FLUSH PRIVILEGES;


```

1.修改字段的长度

语法：

ALTER TABLE 表名 MODIFY COLUMN 字段名 数据类型(修改后的长度)

例子：

将字段的长度由10改为20

ALTER TABLE attence MODIFY COLUMN id INT(20)

2.修改字段的名称

语法：

alter table <表名> change <字段名> <字段新名称> <字段的类型>。

例子：

将字段attence_name改为name

ALTER TABLE attence CHANGE attence_name NAME VARCHAR(20)

3.新增字段

语法：

新增默认为空的字段
ALTER TABLE 表名 ADD COLUMN 字段名 字段类型 DEFAULT NULL;
新增不为空的字段
ALTER TABLE 表名ADD COLUMN 字段名 字段类型 NOT NULL;

例子：
ALTER TABLE attence ADD COLUMN attence_name VARCHAR(20) DEFAULT NULL;

ALTER TABLE attence ADD COLUMN age VARCHAR(20) NOT NULL;

4.删除字段

语法：

ALTER TABLE 表名 DROP COLUMN 字段名;

例子：

ALTER TABLE attence DROP COLUMN age;

5.批量增加字段

方法一
可以使用事务

语法：

begin; //事务开始
alter table 表名 add 字段名 字段类型(长度);
alter table 表名 add 字段名 字段类型(长度);
alter table 表名 add 字段名 字段类型(长度);
alter table 表名 add 字段名 字段类型(长度);
commit;

例子：

begin; //事务开始
alter table em_day_data add f_day_house7 int(11);
alter table em_day_data add f_day_house8 int(11);
alter table em_day_data add f_day_house9 int(11);
alter table em_day_data add f_day_house10 int(11);
commit;

方法二

alter table 表名 add (字段1 类型(长度),字段2 类型(长度),字段3 类型(长度));

alter table em_day_data add (f_day_house11 int(11),f_day_house12 int(11),f_day_house13 int(11));

6.批量修改字段名称

语法：

alter table 表 change 修改前字段名 修改后字段名称 int(11) not null,
change 修改前字段名 修改后字段名称 int(11) not null,
change 修改前字段名 修改后字段名称 int(11) not null,
change 修改前字段名 修改后字段名称 int(11) not null,
change 修改前字段名 修改后字段名称 int(11) not null

例子：

alter table em_day_data change f_day_house11 f_day_hour11 int(11) not null,
change f_day_house12 f_day_hour12 int(11) not null,
change f_day_house13 f_day_hour13 int(11) not null,
change f_day_house14 f_day_hour14 int(11) not null,
change f_day_house15 f_day_hour15 int(11) not null,
change f_day_house16 f_day_hour16 int(11) not null,
change f_day_house17 f_day_hour17 int(11) not null