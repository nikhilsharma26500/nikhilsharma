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
- `CREATE TABLE` is a SQL command used to create a new table.
- `users` is the name of the table.
- `id`, `name`, `email`, `password`, `created_at`, `updated_at`, and `deleted` are the columns in the table.
- `INT`, `VARCHAR(50)`, `TIMESTAMP`, and `BOOLEAN` are the data types of the columns.

Data type definitions:
- <span id="int-definition">`INT`: Integer, can store whole numbers ranging from -2147483648 to 2147483647.</span>

- <span id="varchar-definition">`VARCHAR(50)`: Variable-length character string with a maximum length of 50 characters in our case.</span>
- <span id="unix-timestamp-definition">`UNIX_TIMESTAMP()`: MySQL function that returns current Unix timestamp.</span>
- <span id="tinyint-definition">`TINYINT(1)`: A single-byte integer that is being used as a boolean since `BOOLEAN` is not supported in MySQL.</span>

Constraints used in the query:
- <span id="primary-key-definition">`PRIMARY KEY`: A column or a group of columns that uniquely identifies each row in a table.</span>
- <span id="not-null-definition">`NOT NULL`: Ensures that a column cannot have a NULL value.
- <span id="unique-definition">`UNIQUE`: Ensures that all values in a column are different.
- <span id="default-definition">`DEFAULT`: Specifies a default value for a column when no value is specified.
- <span id="on-update-definition">`ON UPDATE`: Sets the column to the current timestamp when the row is updated.


Let us now create a table named `posts` in the `blog` database:

```sql
CREATE TABLE posts (
    id INT PRIMARY KEY,
    user_id INT NOT NULL,
    title VARCHAR(50) NOT NULL,
    body TEXT NOT NULL,
    created_at TIMESTAMP DEFAULT UNIX_TIMESTAMP(),
    updated_at TIMESTAMP DEFAULT UNIX_TIMESTAMP() ON UPDATE UNIX_TIMESTAMP(),
    deleted TINYINT(1) DEFAULT 0

    FOREIGN KEY (user_id) REFERENCES users(id)
);
```

Let us explain the above SQL query:
- `CREATE TABLE` is a SQL command used to create a new table.
- `posts` is the name of the table.
- `id`, `user_id`, `title`, `body`, `created_at`, `updated_at`, and `deleted` are the columns in the table.
- `INT`, `VARCHAR(50)`, `TEXT`, and `TIMESTAMP` are the data types of the columns.

Data type definitions:
- `INT`: Refer to the [explanation above](#int-definition).
- `VARCHAR(50)`: Refer to the [explanation above](#varchar-definition).
- `TEXT`: A string data type with a variable length. The maximum length is 65,535 characters.
- `UNIX_TIMESTAMP()`: Refer to the [explanation above](#unix-timestamp-definition).
- `TINYINT(1)`: Refer to the [explanation above](#tinyint-definition).
- `FOREIGN KEY`: A FOREIGN KEY is a field (or collection of fields) in one table that refers to the PRIMARY KEY in another table.

Constraints used in the query:
- `PRIMARY KEY`: Refer to the [explanation above](#primary-key-definition).
- `NOT NULL`: Refer to the [explanation above](#not-null-definition).
- `DEFAULT`: Refer to the [explanation above](#default-definition).
- `ON UPDATE`: Refer to the [explanation above](#on-update-definition).
- `REFERENCES`: A constraint that defines a relationship between two tables.