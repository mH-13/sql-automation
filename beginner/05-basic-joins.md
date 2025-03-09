# Basic Joins in SQL

## Introduction
Joins in SQL are used to combine rows from two or more tables based on a related column between them. They are essential for querying data that is spread across multiple tables.

## Types of Joins

### 1. INNER JOIN
An `INNER JOIN` returns records that have matching values in both tables.

**Syntax:**
```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.common_column = table2.common_column;
```

**Use Case:**
Retrieve a list of customers along with their orders.
```sql
SELECT customers.customer_id, customers.name, orders.order_id
FROM customers
INNER JOIN orders
ON customers.customer_id = orders.customer_id;
```

### 2. LEFT JOIN (or LEFT OUTER JOIN)
A `LEFT JOIN` returns all records from the left table (table1), and the matched records from the right table (table2). The result is NULL from the right side if there is no match.

**Syntax:**
```sql
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.common_column = table2.common_column;
```

**Use Case:**
Retrieve all customers and their orders, including customers who have not placed any orders.
```sql
SELECT customers.customer_id, customers.name, orders.order_id
FROM customers
LEFT JOIN orders
ON customers.customer_id = orders.customer_id;
```

### 3. RIGHT JOIN (or RIGHT OUTER JOIN)
A `RIGHT JOIN` returns all records from the right table (table2), and the matched records from the left table (table1). The result is NULL from the left side when there is no match.

**Syntax:**
```sql
SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.common_column = table2.common_column;
```

**Use Case:**
Retrieve all orders and the customers who placed them, including orders that do not have associated customers.
```sql
SELECT customers.customer_id, customers.name, orders.order_id
FROM customers
RIGHT JOIN orders
ON customers.customer_id = orders.customer_id;
```

### 4. FULL JOIN (or FULL OUTER JOIN)
A `FULL JOIN` returns all records when there is a match in either left (table1) or right (table2) table records. It returns NULL for unmatched rows on either side.

**Syntax:**
```sql
SELECT columns
FROM table1
FULL JOIN table2
ON table1.common_column = table2.common_column;
```

**Use Case:**
Retrieve all customers and orders, including those that do not have a match in the other table.
```sql
SELECT customers.customer_id, customers.name, orders.order_id
FROM customers
FULL JOIN orders
ON customers.customer_id = orders.customer_id;
```

### 5. CROSS JOIN
A `CROSS JOIN` returns the Cartesian product of the two tables, i.e., it returns all possible combinations of rows from the tables.

**Syntax:**
```sql
SELECT columns
FROM table1
CROSS JOIN table2;
```

**Use Case:**
Generate a combination of all products and categories.
```sql
SELECT products.product_name, categories.category_name
FROM products
CROSS JOIN categories;
```

### 6. SELF JOIN
A `SELF JOIN` is a regular join but the table is joined with itself.

**Syntax:**
```sql
SELECT a.columns, b.columns
FROM table a, table b
WHERE condition;
```

**Use Case:**
Find pairs of employees who work in the same department.
```sql
SELECT a.employee_id, a.name, b.employee_id, b.name
FROM employees a, employees b
WHERE a.department_id = b.department_id
AND a.employee_id <> b.employee_id;
```

## Conclusion
Joins are a powerful feature in SQL that allow you to retrieve and analyze data from multiple tables. Understanding the different types of joins and their use cases will help you write more efficient and effective SQL queries.


# Claude 

Explanation:

Joins combine data from multiple tables based on related columns. Common types include INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL JOIN.


-- Create a departments table
CREATE TABLE departments (
    id INT PRIMARY KEY,
    name VARCHAR(50)
);

-- Insert data
INSERT INTO departments (id, name)
VALUES (1, 'Sales'), (2, 'Marketing');

-- Inner join
SELECT employees.name, departments.name AS dept_name
FROM employees
INNER JOIN departments ON employees.department = departments.name;

-- Left join
SELECT employees.name, departments.name AS dept_name
FROM employees
LEFT JOIN departments ON employees.department = departments.name;


Use Case:

You’re reporting employee department assignments. An INNER JOIN links employees to their departments, while a LEFT JOIN includes employees without department matches.