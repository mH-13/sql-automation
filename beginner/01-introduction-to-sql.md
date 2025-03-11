# Gork
-- Create a new database
CREATE DATABASE my_database;

-- Use the database
USE my_database;

-- Create a table
**CREATE TABLE employees (**
    **id INT PRIMARY KEY,**
    **name VARCHAR(50),**
    **age INT,**
    **department VARCHAR(50)**
); **

-- Insert data
**INSERT INTO employees (id, name, age, department)**
**VALUES (1, 'John Doe', 30, 'Sales');**

-- Retrieve all data
**SELECT * FROM employees;**


# Brief Discussion

## Introduction to SQL

SQL, or Structured Query Language, is a powerful tool used to communicate with and manipulate databases. Think of a database as a giant, organized library where you can store and retrieve information quickly and efficiently.

### Why Learn SQL?

Learning SQL is like learning how to ask a librarian for the exact book you want. Instead of searching through every shelf, you can simply ask for the book by its title, author, or subject. SQL helps you:

- **Create** databases to store information.
- **Insert** new data into your database.
- **Update** existing data.
- **Delete** data you no longer need.
- **Query** the database to find specific information.

### Basic SQL Commands

Here are some basic SQL commands to get you started:

- **CREATE DATABASE**: creates a new database.
- **USE**:selects the database you want to work with.
- **CREATE TABLE**: creates a new table within the database.
- **INSERT INTO**: adds new data to a table.
- **SELECT**: retrieves data from a table.

### Example

Let's say you want to keep track of employees in a company. You can create a database, add a table for employees, and insert data about each employee. Finally, you can retrieve the data to see all the employees.

By learning SQL, you'll be able to manage and retrieve data efficiently, making it an essential skill for anyone working with databases.

Happy learning!