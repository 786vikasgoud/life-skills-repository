# SQL
## Introduction to SQL
* SQL stands for Structured Query Language. It is a standard language for accessing and manipulating databases.
## SQL Basics
### Creating a Table
* By using the CREATE TABLE key word we can create the table in database.
#### Syntax of the create table:
###### CREATE TABLE table_name.
##### Example :
```
CREATE TABLE employees (
    emp_id INT PRIMARY KEY,
    emp_name VARCHAR(50),
    emp_salary DECIMAL(10, 2),
    department_id INT
);
```
### Inserting Data
*  By using the INSERT INTO key word we can insert the data into the table in database.
#### Syntax for Insert data:
###### INSERT INTO table_name.
##### Example :
```
INSERT INTO employees (emp_id, emp_name, emp_salary, department_id)
VALUES (1, 'John Doe', 50000.00, 101);
```
### Selecting Data
* To select the paticular data from table we will use SELECT key word.
#### Syntax for Selecting data:
###### SELECT * FROM table_name;
##### Example :
```
SELECT emp_name, emp_salary
FROM employees
WHERE department_id = 101;
```
## Joins
### Types of joins
Inner Join
sql
Copy code
SELECT employees.emp_name, departments.department_name
FROM employees
INNER JOIN departments ON employees.department_id = departments.department_id;
Left Join
sql
Copy code
SELECT employees.emp_name, departments.department_name
FROM employees
LEFT JOIN departments ON employees.department_id = departments.department_id;
Aggregations
Count
sql
Copy code
SELECT department_id, COUNT(emp_id) AS emp_count
FROM employees
GROUP BY department_id;
Sum
sql
Copy code
SELECT department_id, SUM(emp_salary) AS total_salary
FROM employees
GROUP BY department_id;
















