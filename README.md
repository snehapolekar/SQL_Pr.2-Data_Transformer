# 🧹 PR.2 – Data Transformer (SQL Project)

## 📌 Project Overview

**Data Transformer** is a MySQL project that demonstrates how to retrieve, combine, filter, transform, and analyze data using SQL queries. It uses customer, order, and employee records to practise joins, subqueries, date functions, string functions, window functions, and conditional statements.

## 🎯 Project Objectives

- Create and manage a relational database using MySQL.
- Connect customer and order records using JOIN operations.
- Retrieve records using subqueries.
- Extract and format date values.
- Clean and transform text using string functions.
- Calculate running totals and rank records.
- Categorize order discounts and employee salary levels.

## 🛠️ Technologies Used

- **Database:** MySQL
- **Language:** SQL
- **Tools:** MySQL Workbench / VS Code with a MySQL extension

## 🗃️ Database Details

**Database name:** `Data_transformer`

The project contains three tables:

### 1. 👥 Customers

| Column | Data type | Description |
|---|---|---|
| `Customer_id` | INT (Primary Key) | Unique customer ID |
| `First_name` | VARCHAR(50) | Customer's first name |
| `Last_name` | VARCHAR(50) | Customer's last name |
| `Email` | VARCHAR(50) | Customer's email address |
| `Registration_date` | DATE | Customer registration date |

### 2. 🛒 Order

| Column | Data type | Description |
|---|---|---|
| `Order_id` | INT (Primary Key) | Unique order ID |
| `Customer_id` | INT (Foreign Key) | References `Customers.Customer_id` |
| `Order_date` | DATE | Date of the order |
| `Total_amount` | DECIMAL(10,2) | Total order amount |

### 3. 🧑‍💼 Employees

| Column | Data type | Description |
|---|---|---|
| `Employee_id` | INT (Primary Key) | Unique employee ID |
| `First_name` | VARCHAR(50) | Employee's first name |
| `Last_name` | VARCHAR(50) | Employee's last name |
| `Department` | VARCHAR(50) | Employee department |
| `Hire_date` | DATE | Employee joining date |
| `Salary` | DECIMAL(10,2) | Employee salary |

## 🔗 Table Relationship

- One customer can place multiple orders.
- `Customers.Customer_id` is the primary key.
- `Order.Customer_id` is a foreign key referencing the Customers table.
- The Employees table stores employee information separately.

## 📚 SQL Queries Covered

| Query | Topic | Description |
|---|---|---|
| Q1 | INNER JOIN | Displays orders with matching customer details |
| Q2 | LEFT JOIN | Displays all customers and their orders, if available |
| Q3 | RIGHT JOIN | Displays all customers and matching order details |
| Q4 | FULL OUTER JOIN | Combines left and right join results using `UNION` |
| Q5 | Subquery | Finds customers with orders above the average order amount |
| Q6 | Subquery | Finds employees with salaries greater than or equal to the average salary |
| Q7 | Date Functions | Extracts the year and month from order dates |
| Q8 | `DATEDIFF()` | Calculates the number of days between an order date and today |
| Q9 | `DATE_FORMAT()` | Formats dates as DD-MM-YYYY |
| Q10 | `CONCAT()` and `TRIM()` | Combines employee first and last names |
| Q11 | `REPLACE()` | Replaces `gmail.com` with `yahoo.com` in email addresses |
| Q12 | `UPPER()` and `LOWER()` | Changes first names to uppercase and last names to lowercase |
| Q13 | `TRIM()` | Removes extra spaces from email values |
| Q14 | Window Function | Calculates a running total of order amounts |
| Q15 | `RANK()` | Ranks orders by total amount in descending order |
| Q16 | `CASE` | Assigns discounts based on order amounts |
| Q17 | `CASE` | Categorizes employee salaries as Low, Medium, or High |

## ▶️ How to Run the Project

1. Install and open MySQL Workbench or another MySQL-compatible SQL editor.
2. Connect to your MySQL server.
3. Open the project SQL file.
4. Run the database creation statement:
   ```sql
   CREATE DATABASE IF NOT EXISTS Data_transformer;
   USE Data_transformer;
   ```
5. Create the `Customers`, `Order`, and `Employees` tables.
6. Insert the sample records.
7. Execute Q1–Q17 one by one to view the results.

> ⚠️ **First-run note:** The script contains `DELETE FROM \`Order\`;` before the `Order` table is created. On a fresh database, this statement will fail because the table does not exist yet. Run that DELETE statement only after creating the `Order` table, or skip it on the first run. The statement is useful when resetting existing order data.

## 💡 Key SQL Concepts Practised

- Database and table creation
- Primary keys and foreign keys
- INSERT and DELETE statements
- INNER, LEFT, and RIGHT JOIN
- UNION
- Nested subqueries
- Aggregate functions such as `AVG()` and `SUM()`
- Date and string functions
- Window functions
- Conditional logic with `CASE`

## 🌟 Learning Outcomes

After completing this project, you will have practical experience in:

- Working with related tables in a relational database.
- Writing SQL queries to retrieve and transform data.
- Applying functions to dates, numbers, and strings.
- Analysing records with ranking and running totals.
- Using conditional logic to classify data.

## 👩‍💻 Author

Linkedin id : www.linkedin.com/in/sneha-polekar-1a8022415

Gmail id : snehapolekar26@gmail.com

---

⭐ *This project was created for SQL practice and learning as part of PR.2 – Data Transformer.*
