---
title: Intro to SEQUEL aka SQL
draft: false
tags:
---

## What is SQL?

SQL stands for Structured Query Language. It is a language used to interact with [relational databases](https://nikhilsharma.xyz/Databases/Relational_Databases/Intro-to-Relational-Databases). SQL is used to perform tasks such as updating data on a database, or retrieving data from a database. It is a standard language for relational database management systems.

Let us try to understand SQL with an example of a blogging site in MySQL.

Here is how we can create a database named `blog`:

```sql
CREATE DATABASE blog;
```

Now, we will create a table named `users` in the `blog` database:

```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    email VARCHAR(50) NOT NULL UNIQUE,
    password VARCHAR(50) NOT NULL,
    created_at TIMESTAMP DEFAULT UNIX_TIMESTAMP(),
    updated_at TIMESTAMP DEFAULT UNIX_TIMESTAMP() ON UPDATE UNIX_TIMESTAMP(),
    deleted TINYINT(1) DEFAULT 0
);
```

Let us explain the above SQL query:
- `CREATE TABLE` is a SQL command used to create a new table
- `users` is the name of the table
- `id`, `name`, `email`, `password`, `created_at`, `updated_at`, and `deleted` are the columns in the table
- `INT`, `VARCHAR(50)`, `TIMESTAMP`, and `BOOLEAN` are the data types of the columns

Data type definitions:
- `INT`: Integer, can store whole numbers ranging from -2147483648 to 2147483647
- `VARCHAR(50)`: Variable-length character string with a maximum length of 50 characters in our case
- `UNIX_TIMESTAMP()`: MySQL function that returns current Unix timestamp
- `TINYINT(1)`: A single-byte integer that is being used as a boolean since `BOOLEAN` is not supported in MySQL.

