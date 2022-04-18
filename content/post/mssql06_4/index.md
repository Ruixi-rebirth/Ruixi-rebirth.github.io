---
title: "Mssql06_4"
date: 2022-04-18T22:32:02+08:00
tags:
  - Mssql
categories:
  - Devops
image: feature.jpg
math: true
draft: false
---

## TRUNCATE

truncate 的作用是清空表或者说是截断表，只能作用于表;会清空表中的所有行，但表结构及其约束、索引等保持不变(**empty for reuse**)

### 语法

```SQL
TRUNCATE TABLE  table_name;
table_name: Name of the table to be truncated.
```
