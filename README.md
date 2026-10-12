# Week 2 Assignment: Introduction to SQL

## Description
This assignment covers the fundamentals of SQL using the `sales` database. It demonstrates how to retrieve, filter, sort, and limit records from different database tables using SQL queries.

## Learning Objectives
- Retrieve specific columns using `SELECT`.
- Filter records using `WHERE`.
- Sort query results using `ORDER BY`.
- Limit the number of results using `LIMIT`.
- Retrieve all columns and records using `SELECT *`.

## Assignment Questions

### Question 1: Retrieve Payment Information
Retrieve the check number, payment date, and amount from the `payments` table.

```sql
SELECT checkNumber, paymentDate, amount
FROM payments;
```

### Question 2: Find Orders in Process
Retrieve orders with the status `In Process`, sorted by order date in descending order.

```sql
SELECT orderDate, requiredDate, status
FROM orders
WHERE status = 'In Process'
ORDER BY orderDate DESC;
```

### Question 3: Find Sales Representatives
Retrieve the first name, last name, and email of employees whose job title is `Sales Rep`, sorted by employee number in descending order.

```sql
SELECT firstName, lastName, email
FROM employees
WHERE jobTitle = 'Sales Rep'
ORDER BY employeeNumber DESC;
```

### Question 4: Retrieve Office Information
Retrieve all columns and records from the `offices` table.

```sql
SELECT *
FROM offices;
```

### Question 5: Retrieve the Five Cheapest Products
Retrieve the product name and quantity in stock for the five products with the lowest buying prices.

```sql
SELECT productName, quantityInStock
FROM products
ORDER BY buyPrice ASC
LIMIT 5;
```

## Database Used
- Database: `sales`
- Database Management System: MySQL
- Tool: MySQL Workbench

## How to Run
1. Import the `sales` database into MySQL if it is not already available.
2. Open MySQL Workbench and connect to the local MySQL server.
3. Select the database using `USE sales;`.
4. Run the SQL queries in the editor.

## Conclusion
This assignment provided practical experience with basic SQL commands for retrieving, filtering, sorting, and limiting data in a relational database.
