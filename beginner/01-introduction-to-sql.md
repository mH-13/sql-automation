-- Create a new database
CREATE DATABASE my_database;

-- Use the database
USE my_database;

-- Create a table
CREATE TABLE employees (
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    department VARCHAR(50)
);

-- Insert data
INSERT INTO employees (id, name, age, department)
VALUES (1, 'John Doe', 30, 'Sales');

-- Retrieve all data
SELECT * FROM employees;