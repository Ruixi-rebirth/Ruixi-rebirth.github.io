---
title: "Mssql06_3"
date: 2022-04-18T22:31:58+08:00
tags:
  - Mssql
categories:
  - Devops
image: feature.jpg
math: true
draft: false
---

## ALTER

ALTER TABLE 用于添加、删除/删除或修改现有表中的列。 它还用于在现有表上添加和删除各种约束

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
