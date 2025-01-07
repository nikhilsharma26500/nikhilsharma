---
title: Intro to SEQUEL aka SQL
draft: false
tags:
---

## What is SQL?

SQL stands for Structured Query Language. It is a language used to interact with ![relational databases](https://nikhilsharma.xyz/Databases/Relational_Databases/Intro-to-Relational-Databases). SQL is used to perform tasks such as updating data on a database, or retrieving data from a database. It is a standard language for relational database management systems.

## SQL Commands

### CREATE DATABASE

The CREATE DATABASE statement is used to create a new SQL database.

```sql
CREATE DATABASE database_name;
```

### DROP DATABASE

The DROP DATABASE statement is used to delete a SQL database.

```sql
DROP DATABASE database_name;
```

### CREATE TABLE

The CREATE TABLE statement is used to create a new table in a database.

```sql
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype,
    ...
);
```

### DROP TABLE

The DROP TABLE statement is used to delete a table in a database.

```sql
DROP TABLE table_name;
```

### SELECT

The SELECT statement is used to select data from a database. The data returned is stored in a result table, called the result-set.

```sql
SELECT column1, column2, ...
FROM table_name;
```

#### SELECT DISTINCT

The SELECT DISTINCT statement is used to return only distinct (different) values.

```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

### WHERE

The WHERE clause is used to filter records. The WHERE clause is used to extract only those records that fulfill a specified condition.

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

### AND, OR, NOT`

The AND, OR, and NOT operators are used to filter records based on more than one condition.

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2;
```

### ORDER BY

The ORDER BY keyword is used to sort the result-set in ascending or descending order.

```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ... ASC|DESC;
```

### INSERT INTO

The INSERT INTO statement is used to insert new records in a table.

```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

### UPDATE

The UPDATE statement is used to modify the existing records in a table.

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

### DELETE

The DELETE statement is used to delete existing records in a table.

```sql
DELETE FROM table_name
WHERE condition;
```

### ALTER TABLE

The ALTER TABLE statement is used to add, delete, or modify columns in an existing table.

```sql
ALTER TABLE table_name
ADD column_name datatype;
```
