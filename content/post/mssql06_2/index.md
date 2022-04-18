---
title: "Mssql06_2"
date: 2022-04-18T22:31:51+08:00
tags:
  - Mssql
categories:
  - Devops
image: feature.jpg
math: true
draft: false
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
