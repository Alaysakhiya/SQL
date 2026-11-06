# 🛒 E-Commerce Database Management System

<p align="center">
  <img src="https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
  <img src="https://img.shields.io/badge/SQL-Queries-orange?style=for-the-badge&logo=postgresql&logoColor=white">
  <img src="https://img.shields.io/badge/Project-Database%20Management-blue?style=for-the-badge">
</p>

## 📌 About The Project

The **E-Commerce Database Management System** is a MySQL-based database project designed to manage customers, orders, products, and order details efficiently.

This project demonstrates practical SQL skills through database operations, data manipulation, filtering, aggregate functions, and table relationships using JOIN operations.

## 🗄️ Database Tables

The project consists of four main tables:

| Table Name | Description | Records |
|---|---|---:|
| 👤 CUSTOMER | Stores customer information | 5 |
| 📦 ORDERS | Maintains customer order records | 15 |
| 🛍️ PRODUCTS | Stores product details, prices, and stock | 15 |
| 📋 ORDER_DETAILS | Maintains individual order items and subtotals | 15 |

## ⚡ SQL Concepts Implemented

### 1. Data Manipulation (DML)
- `INSERT` – Add customer, order, product, and order detail records.
- `UPDATE` – Modify existing customer addresses and product prices.
- `DELETE` – Remove customer, order, and out-of-stock product records.

### 2. Data Retrieval (DQL)
- `SELECT` – Retrieve records from database tables.
- `WHERE` – Filter records using specific conditions.
- `BETWEEN` – Retrieve products within a particular price range.
- `ORDER BY` – Sort products by price.
- `LIMIT` – Retrieve the top three records.

### 3. Aggregate Functions
- `MAX()` – Find the highest order amount or product price.
- `MIN()` – Find the lowest order amount or product price.
- `AVG()` – Calculate the average order amount.
- `SUM()` – Calculate total revenue.
- `COUNT()` – Count products sold.

### 4. Advanced SQL Operations
- `INNER JOIN` / `RIGHT JOIN` – Combine related table records.
- `GROUP BY` – Group product sales.
- `DATEDIFF()` – Calculate the difference between order dates and the current date.
- `DATE()` and `NOW()` – Work with date and time values.

## 📊 Key Database Insights

Some important results obtained from the SQL queries:

| Analysis | Result |
|---|---:|
| Total Customers | 5 |
| Total Orders | 15 |
| Total Products Initially | 15 |
| Total Order Details | 15 |
| Highest Order Amount | ₹55,000 |
| Lowest Order Amount | ₹12,000 |
| Average Order Amount | ₹28,214.29 |
| Total Revenue (Order Details) | ₹9,05,000 |
| Products Deleted (Out of Stock) | 2 |

## 🔍 Example SQL Queries

**1. Find the most expensive and cheapest products**

```sql
SELECT
    MAX(PRICE) AS EXPENSIVE,
    MIN(PRICE) AS CHEAPEST
FROM PRODUCTS;
```

**2. Calculate total revenue**

```sql
SELECT SUM(SUB_TOTAL) AS TOTAL_REVENUE
FROM ORDER_DETAILS;
```

**3. Find the top 3 orders by quantity**

```sql
SELECT *
FROM ORDER_DETAILS
ORDER BY QUANTITY DESC
LIMIT 3;
```

**4. Find total products sold**

```sql
SELECT
    P.PRODUCT_ID,
    P.PRODUCT_NAME,
    COUNT(O.PRODUCT_ID) AS TOTAL_SOLD
FROM PRODUCTS AS P
RIGHT JOIN ORDER_DETAILS AS O
ON P.PRODUCT_ID = O.PRODUCT_ID
GROUP BY P.PRODUCT_ID, P.PRODUCT_NAME;
```

## 🛠️ Technologies Used

<p>
  <img src="https://skillicons.dev/icons?i=mysql" height="50" />
</p>

- **Database:** MySQL
- **Language:** SQL
- **Environment:** MySQL Command Line / MySQL Workbench

## 🎯 Learning Outcomes

Through this project, I practiced:

- Designing and managing relational database tables.
- Performing CRUD operations.
- Writing SQL queries with multiple conditions.
- Applying aggregate functions for data analysis.
- Working with JOIN operations and table relationships.
- Analyzing product sales, revenue, and order information.
- Performing date-based calculations.

---

<p align="center">
  <b>💻 Practicing SQL | Building Database Skills | Learning Through Projects</b>
</p>