# Filtering Data in SQL

Filtering data is a fundamental aspect of querying databases in SQL. It allows you to retrieve only the rows that meet certain criteria, making your queries more efficient and your results more relevant.

## Basic Filtering with `WHERE`

The `WHERE` clause is used to filter records based on specified conditions. The basic syntax is:

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

### Example

```sql
SELECT * FROM employees
WHERE department = 'Sales';
```

This query retrieves all employees who work in the Sales department.

## Using Comparison Operators

Comparison operators are used to filter data based on specific conditions. Common operators include:

- `=` : Equal to
- `!=` or `<>` : Not equal to
- `>` : Greater than
- `<` : Less than
- `>=` : Greater than or equal to
- `<=` : Less than or equal to

### Example

```sql
SELECT * FROM products
WHERE price > 100;
```

This query retrieves all products with a price greater than 100.

## Filtering with Logical Operators

Logical operators allow you to combine multiple conditions. The most common logical operators are:

- `AND` : All conditions must be true
- `OR` : At least one condition must be true
- `NOT` : Negates a condition

### Example

```sql
SELECT * FROM orders
WHERE status = 'Shipped' AND order_date >= '2023-01-01';
```

This query retrieves all orders that have been shipped and were placed on or after January 1, 2023.

## Using `IN` and `BETWEEN`

The `IN` operator allows you to specify multiple values in a `WHERE` clause. The `BETWEEN` operator filters data within a range of values.

### Example with `IN`

```sql
SELECT * FROM customers
WHERE country IN ('USA', 'Canada', 'Mexico');
```

This query retrieves all customers from the USA, Canada, or Mexico.

### Example with `BETWEEN`

```sql
SELECT * FROM transactions
WHERE amount BETWEEN 100 AND 500;
```

This query retrieves all transactions with an amount between 100 and 500.

## Filtering with `LIKE` for Pattern Matching

The `LIKE` operator is used for pattern matching with wildcard characters:

- `%` : Represents zero or more characters
- `_` : Represents a single character

### Example

```sql
SELECT * FROM employees
WHERE first_name LIKE 'J%';
```

This query retrieves all employees whose first name starts with the letter 'J'.

## Filtering with `IS NULL` and `IS NOT NULL`

To filter records with `NULL` values, use the `IS NULL` or `IS NOT NULL` operators.

### Example

```sql
SELECT * FROM orders
WHERE delivery_date IS NULL;
```

This query retrieves all orders that do not have a delivery date.

## Combining Filters

You can combine multiple filtering techniques to create complex queries.

### Example

```sql
SELECT * FROM products
WHERE category = 'Electronics' AND (price BETWEEN 100 AND 500) AND stock > 0;
```

This query retrieves all electronic products priced between 100 and 500 that are in stock.

## Conclusion

Filtering data in SQL is a powerful way to retrieve specific subsets of data from your database. By using the `WHERE` clause along with various operators and conditions, you can create precise and efficient queries to meet your data retrieval needs.


# claude 
Explanation:

The WHERE clause filters rows based on conditions, using operators like =, >, BETWEEN, and AND.

-- Filter by exact match
SELECT * FROM employees WHERE department = 'Sales';

-- Filter by range
SELECT * FROM employees WHERE age BETWEEN 25 AND 35;

-- Filter with multiple conditions
SELECT * FROM employees WHERE age > 25 AND department = 'Sales';


Use Case:

You’re analyzing Sales team performance and need employees aged 25–35. A filtered SELECT query identifies this group.