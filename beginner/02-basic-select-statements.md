# Basic SELECT Statements in SQL

The `SELECT` statement is used to query the database and retrieve data from one or more tables. Here are the key components and examples of using the `SELECT` statement:

## Basic Syntax

```sql
SELECT column1, column2, ...
FROM table_name;
```

- `column1, column2, ...` are the names of the columns you want to retrieve.
- `table_name` is the name of the table from which to retrieve the data.

## Selecting All Columns: To select all columns from a table, use the `*` wildcard:

```sql
SELECT * FROM table_name;
```

## Using WHERE Clause - The `WHERE` clause is used to filter records:

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

Example:

```sql
SELECT * FROM employees
WHERE department = 'Sales';
```

## Using ORDER BY Clause:  The `ORDER BY` clause is used to sort the result set:

```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1 [ASC|DESC];
```

Example:

```sql
SELECT * FROM employees
ORDER BY last_name ASC;
```

## Using DISTINCT Keyword:  The `DISTINCT` keyword is used to return only distinct (different) values:

```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

Example:

```sql
SELECT DISTINCT department
FROM employees;
```

## Using LIMIT Clause: The `LIMIT` clause is used to specify the number of records to return:

```sql
SELECT column1, column2, ...
FROM table_name
LIMIT number;
```

Example:

```sql
SELECT * FROM employees
LIMIT 10;
```

## Combining Conditions with AND, OR:  You can combine multiple conditions using `AND` and `OR`:

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition1 AND condition2;
```

Example:

```sql
SELECT * FROM employees
WHERE department = 'Sales' AND salary > 50000;
```

## Using Aliases: Aliases are used to give a table or a column a temporary name:

```sql
SELECT column_name AS alias_name
FROM table_name;
```

Example:

```sql
SELECT first_name AS fname, last_name AS lname
FROM employees;
```

## Joining Tables: To retrieve data from multiple tables, you can use JOIN operations:

```sql
SELECT columns
FROM table1
JOIN table2
ON table1.column = table2.column;
```

Example:

```sql
SELECT employees.first_name, departments.department_name
FROM employees
JOIN departments
ON employees.department_id = departments.department_id;
```

These are the basics of the `SELECT` statement in SQL. With these tools, you can perform a wide variety of queries to retrieve and manipulate data in your database.


## Code Example
-- Select specific columns
# SELECT name, age FROM employees;

-- Select all columns
# SELECT * FROM employees;

-- Select with a condition
# SELECT * FROM employees WHERE age > 25;

# Use Case:

You need a list of employees over 25 years old for a benefits program. A SELECT statement with a WHERE clause retrieves this data efficiently.