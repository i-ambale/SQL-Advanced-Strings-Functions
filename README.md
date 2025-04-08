# SQL Advanced String Functions
© ExploreAI Academy

📘 Overview
This project explores advanced SQL string functions and their application in solving real-world data manipulation problems. It uses the Northwind.db SQLite database to demonstrate powerful techniques in handling, transforming, and analyzing string data.
---
## 🎯 Learning Objectives
By the end of this exercise, you should be able to:

- Apply SQL functions for data type conversion using `CAST()` and related functions.

- Handle NULL values effectively with functions like `COALESCE()`.

- Use string manipulation techniques such as `SUBSTRING()`, `REPLACE()`, `TRIM()`, and `CONCAT()` (or its SQLite equivalent using ||) to clean, extract, and modify text data.

- Solve complex string handling problems using nested and combined SQL functions.
--- 
## 🗂️ Prerequisites
- A working installation of SQLite or an environment that connects to Northwind.db.

- Basic to intermediate knowledge of SQL.

- Understanding of SQL window functions, joins, and aggregate functions is helpful but not required.
---
## 🧪 Database Used
- **Northwind.db**
    This is a sample retail database representing a company's data including Customers, Orders, Employees, Products, and more.
---
### 🛠️ Key SQL Functions Explored

| **Function**           | **Purpose**                                                        | **Example (SQLite)**                                                                 |
|------------------------|---------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| `CAST()`               | Convert one data type to another                                    | `SELECT CAST(Salary AS TEXT) FROM Employees;`                                       |
| `COALESCE()`           | Replace `NULL` values with a default                                | `SELECT COALESCE(ContactTitle, 'N/A') FROM Customers;`                              |
| `SUBSTR()`             | Extract a part of a string                                          | `SELECT SUBSTR(OrderDate, 1, 7) AS YearMonth FROM Orders;`                          |
| `REPLACE()`            | Replace part of a string with another                               | `SELECT REPLACE(Phone, '-', ' ') FROM Customers;`                                   |
| `TRIM()`               | Remove whitespace or specified characters                           | `SELECT TRIM('   ExploreAI   ') AS CleanText;`                                      |
| `UPPER()` / `LOWER()`  | Convert string to upper or lower case                               | `SELECT UPPER(FirstName) FROM Employees;`                                           |
| `||` (concat operator) | Concatenate strings in SQLite                                       | `SELECT FirstName || ' ' || LastName AS FullName FROM Employees;`                  |
| `LENGTH()`             | Get the length of a string                                          | `SELECT LENGTH(CompanyName) FROM Customers;`                                        |
| `INSTR()`              | Find the position of a substring                                    | `SELECT INSTR(ContactName, ' ') AS SpacePosition FROM Customers;`                  |
| `IFNULL()`             | Return alternate value if the first is NULL (SQLite's COALESCE)     | `SELECT IFNULL(Region, 'Not Provided') FROM Customers;`                            |
---
## 📊 Example Use Cases
- Standardizing country names by removing parenthetical text

- Creating custom IDs by combining multiple columns

- Extracting first names from full name fields

- Replacing NULLs in text fields for cleaner analytics

- Formatting strings for reports and dashboards
---
## ✅ How to Run
1. Ensure you have SQLite installed or use a SQL-compatible environment like DB Browser for SQLite or Jupyter Notebook with %sql magic.
2. Load Northwind.db into your environment.
3. Run the SQL queries provided in the notebook or scripts, experimenting with different functions as you go.
---
## 📌 Notes
- SQLite uses `||` instead of `CONCAT()` for combining strings.

- Always check for NULLs before performing string operations.

- For debugging and testing string results, use `SELECT` statements with `LIMIT`.
---
## 📚 References
SQLite String Functions

ExploreAI Academy SQL Curriculum
---
### 🛠️ Key SQL Functions Explored

| **Function**           | **Purpose**                                                        | **Example (SQLite)**                                                                 |
|------------------------|---------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| `CAST()`               | Convert one data type to another                                    | `SELECT CAST(Salary AS TEXT) FROM Employees;`                                       |
| `COALESCE()`           | Replace `NULL` values with a default                                | `SELECT COALESCE(ContactTitle, 'N/A') FROM Customers;`                              |
| `SUBSTR()`             | Extract a part of a string                                          | `SELECT SUBSTR(OrderDate, 1, 7) AS YearMonth FROM Orders;`                          |
| `REPLACE()`            | Replace part of a string with another                               | `SELECT REPLACE(Phone, '-', ' ') FROM Customers;`                                   |
| `TRIM()`               | Remove whitespace or specified characters                           | `SELECT TRIM('   ExploreAI   ') AS CleanText;`                                      |
| `UPPER()` / `LOWER()`  | Convert string to upper or lower case                               | `SELECT UPPER(FirstName) FROM Employees;`                                           |
| `||`                   | Concatenate strings in SQLite                                       | `SELECT FirstName || ' ' || LastName AS FullName FROM Employees;`                  |
| `LENGTH()`             | Get the length of a string                                          | `SELECT LENGTH(CompanyName) FROM Customers;`                                        |
| `INSTR()`              | Find the position of a substring                                    | `SELECT INSTR(ContactName, ' ') AS SpacePosition FROM Customers;`                   |
| `IFNULL()`             | Return alternate value if the first is NULL (SQLite's COALESCE)     | `SELECT IFNULL(Region, 'Not Provided') FROM Customers;`                            |


### 🛠️ Key SQL Functions Explored

| **Function**           | **Purpose**                                                        | **Example (SQLite)**                                                                 |
|------------------------|---------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| `CAST()`               | Convert one data type to another                                    | `SELECT CAST(Salary AS TEXT) FROM Employees;`                                       |
| `COALESCE()`           | Replace `NULL` values with a default                                | `SELECT COALESCE(ContactTitle, 'N/A') FROM Customers;`                              |
| `SUBSTR()`             | Extract a part of a string                                          | `SELECT SUBSTR(OrderDate, 1, 7) AS YearMonth FROM Orders;`                          |
| `REPLACE()`            | Replace part of a string with another                               | `SELECT REPLACE(Phone, '-', ' ') FROM Customers;`                                   |
| `TRIM()`               | Remove whitespace or specified characters                           | `SELECT TRIM('   ExploreAI   ') AS CleanText;`                                      |
| `UPPER()` / `LOWER()`  | Convert string to upper or lower case                               | `SELECT UPPER(FirstName) FROM Employees;`                                           |
| &#124;&#124;           | Concatenate strings in SQLite                                       | SELECT FirstName &#124;&#124; ' ' &#124;&#124; LastName AS FullName FROM Employees; |
| `LENGTH()`             | Get the length of a string                                          | `SELECT LENGTH(CompanyName) FROM Customers;`                                        |
| `INSTR()`              | Find the position of a substring                                    | `SELECT INSTR(ContactName, ' ') AS SpacePosition FROM Customers;`                   |
| `IFNULL()`             | Return alternate value if the first is NULL (SQLite's COALESCE)     | `SELECT IFNULL(Region, 'Not Provided') FROM Customers;`                            |
