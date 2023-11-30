# SQL
## Introduction to SQL
* SQL stands for Structured Query Language. It is a standard language for accessing and manipulating databases.
## SQL Basics
### Creating a Table
* By using the CREATE TABLE key word we can create the table in database.
#### Syntax of the create table :-
###### CREATE TABLE table_name.
##### Example :- 
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
#### Syntax for Insert data :-
###### INSERT INTO table_name.
##### Example :-
```
INSERT INTO employees (emp_id, emp_name, emp_salary, department_id)
VALUES (1, 'John Doe', 50000.00, 101);
```
### Selecting Data
* To select the paticular data from table we will use SELECT key word.
#### Syntax for Selecting Data :- 
###### SELECT * FROM table_name;
##### Example :-
```
SELECT emp_name, emp_salary
FROM employees
WHERE department_id = 101;
```

## Joins
### Types of joins
##### 1) Inner Join.
##### 2) Left Join.
##### 3) RIGHT JOIN.
##### 4) Self Join.
##### 5) FULL JOIN.

#### Inner Join
* The INNER JOIN keyword selects records that have matching values in both tables.
#### Syntax for Inner Join :-
```
SELECT column_name(s)
FROM table1
INNER JOIN table2
ON table1.column_name = table2.column_name;
```
##### Example :-
```
SELECT employees.emp_name, departments.department_name
FROM employees
INNER JOIN departments ON employees.department_id = departments.department_id;
```
#### Left Join
* The LEFT JOIN keyword returns all records from the left table, and the matching records from the right table.
#### Syntax for Left Join :-
```
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name = table2.column_name;
```
 ##### Example :-
 ```
SELECT employees.emp_name, departments.department_name
FROM employees
LEFT JOIN departments ON employees.department_id = departments.department_id;
```
#### Right Join
* The RIGHT JOIN keyword returns all records from the right table, and the matching records from the left table.
#### Syntax for Right Join :-
```
SELECT column_name(s)
FROM table1
RIGHT JOIN table2
ON table1.column_name = table2.column_name;
```
##### Example :-
 ```
SELECT employees.emp_name, departments.department_name
FROM employees
RIGHT JOIN departments ON employees.department_id = departments.department_id;
```

## Aggregations
* MySQL's aggregate function is used to perform calculations on multiple values and return the result in a single value.
#### Syntax :-
```
function_name (DISTINCT | ALL expression)
```
### MySQL Aggregate Functions 
#### count() :-	
* It returns the number of rows, including rows with NULL values in a group.
#### sum() :-	
* It returns the total summed values (Non-NULL) in a set.
#### average() :-
* It returns the average value of an expression.
#### min() :-	
* It returns the minimum (lowest) value in a set.
#### max() :-	
* It returns the maximum (highest) value in a set.
#### groutp_concat() :-	
* It returns a concatenated string.
#### first() :-	
* It returns the first value of an expression.
#### last()	:-
* It returns the last value of an expression.
### COUNT() :-
#### Example :-
```
SELECT department_id, COUNT(emp_id) AS emp_count
FROM employees
GROUP BY department_id;
```
### Sum() :-
#### Example :-
```
SELECT department_id, SUM(emp_salary) AS total_salary
FROM employees
GROUP BY department_id;
```
## Conclusion :
###### Understanding SQL basics, joins, and aggregations is crucial for effective database management. These code samples provide a foundation for ###### querying, combining data, and performing calculations within a relational database system.

## References :-
* [w3schools SQL](https://www.w3schools.com/sql/default.asp)
* [javatpoint SQL](https://www.javatpoint.com/mysql-tutorial)
* [youtube link](https://www.youtube.com/watch?v=hlGoQC332VM)

















