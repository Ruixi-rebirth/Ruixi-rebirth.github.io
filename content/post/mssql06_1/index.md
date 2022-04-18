---
title: "Mssql06_1"
date: 2022-04-18T17:55:28+08:00
tags:
  - Mssql
categories:
  - Devops
image: feature.jpg
math: true
draft: false
---

> [SQL 中有两个可用的 CREATE 语句：](#create)
>
> - **创建数据库**
> - **创建表**

---

## 创建数据库

数据库 被定义为一组结构化的数据,因此，在 SQL 中，以结构良好的方式存储数据的第一步是创建数据库。

### 语法

```SQL
CREATE DATABASE database_name;
```

### 示例

```SQL
CREATE DATABASE StudentScore;
```

## 创建表

我们已经在上面了解了创建数据库。 现在要存储数据，我们需要一个表来执行此操作。 CREATE TABLE 语句用于在 SQL 中创建表。 我们知道一个表由行和列组成。 因此，在创建表时，我们必须向 SQL 提供有关列名、要存储在列中的数据类型、数据大小等所有信息。现在让我们深入了解如何使用 CREATE TABLE 语句创建 SQL 中的表。

### 语法

```SQL
CREATE TABLE table_name
(
column1 data_type(size),
column2 data_type(size),
column3 data_type(size),
....
);
```

### 示例

```SQl
CREATE TABLE Students
(
Sno int(3),
Sname varchar(20),
Sage varchar(20),
);
```

---

## [DROP](#drop)

DROP 用于删除整个数据库或仅删除一个表。DROP 语句会破坏现有数据库、表、索引或视图等对象。

### 语法

```SQL
DROP object object_name

Examples:
DROP TABLE table_name;
table_name: Name of the table to be deleted.

DROP DATABASE database_name;
database_name: Name of the database to be deleted.
```

---

> [ALTER TABLE 用于添加、删除/删除或修改现有表中的列。 它还用于在现有表上添加和删除各种约束](#alter)

## 更改表 - 添加

ADD 用于将列添加到现有表中。 有时我们可能需要添加额外的信息，在这种情况下我们不需要再次创建整个数据库， ADD 来拯救我们

### 语法

```SQL
 ALTER TABLE table_name
    ADD (
    Columnname_1  datatype,
    Columnname_2  datatype,
    …
    Columnname_n  datatype
    );
```

## 更改表 - 删除

### 语法

DROP COLUMN 用于删除表中的列

```SQL
ALTER TABLE table_name
DROP COLUMN column_name;
```

## 改变表 - 修改

它用于修改表中的现有列

### 语法

Syntax(Oracle,MySQL,MariaDB):

```SQL
ALTER TABLE table_name
MODIFY column_name column_type;
```

Syntax(SQL Server):

```SQL
ALTER TABLE table_name
ALTER COLUMN column_name column_type;
```

---

## [TRUNCATE](#truncate)

truncate 的作用是清空表或者说是截断表，只能作用于表;会清空表中的所有行，但表结构及其约束、索引等保持不变(**empty for reuse**)

### 语法

```SQL
TRUNCATE TABLE  table_name;
table_name: Name of the table to be truncated.
```

---

## [DELETE](#delete)

SQL 中的 DELETE 语句用于从表中删除现有记录。 根据我们在 WHERE 子句中指定的条件，我们可以删除单个记录或多个记录。

### 基本语法

```SQL
DELETE FROM table_name WHERE some_condition;

table_name: name of the table
some_condition: condition to choose particular record.
```

### 示例

![](./delete.jpg)

```SQL
DELETE FROM Student WHERE NAME = 'Ram';
```

Output:

| Sno | Sname | Saddress | Sphone | Sage |
| :-: | :---: | :------: | :----: | :--: |
|  2  | Rash  |   Aaa    | xxxxxx |  18  |
|  3  | Stuff |   Bbb    | xxxxxx |  20  |
|  4  |  Sbt  |   Ccc    | xxxxxx |  18  |
|  5  | Chen  |   Ddd    | xxxxxx |  20  |
|  6  | Fres  |   Eee    | xxxxxx |  18  |

```SQL
DELETE FROM Student WHERE Age = 20;
```

Output:

| Sno | Sname | Saddress | Sphone | Sage |
| :-: | :---: | :------: | :----: | :--: |
|  1  |  Ram  |  Delhi   | xxxxxx |  18  |
|  2  | Rash  |   Aaa    | xxxxxx |  18  |
|  4  |  Sbt  |   Ccc    | xxxxxx |  18  |
|  6  | Fres  |   Eee    | xxxxxx |  18  |

删除所有记录？

```SQL
DELETE FROM Student;
```
