# 📊 Sales Data Warehouse and Business Intelligence System

## Project Overview

This project is a SQL-based Sales Data Warehouse designed for a retail company. It centralizes sales data from multiple stores and enables business analysis through advanced SQL queries.

The project demonstrates database design, normalization, SQL programming, and business intelligence concepts.

---

## Objectives

- Design a relational database
- Apply database normalization (1NF, 2NF, 3NF)
- Create relationships using primary and foreign keys
- Populate the database with realistic data
- Perform business analysis using SQL
- Optimize queries using indexes
- Create views, stored procedures, and triggers

---

## Technologies Used

- MySQL
- SQL
- Git
- GitHub
- Excel/CSV
- Power BI (Optional)

---

## Database Schema

### Tables

- Customers
- Products
- Suppliers
- Stores
- Employees
- Orders
- Order_Items

---

## Entity Relationship Diagram

(Add a screenshot of your ER Diagram here.)

Example:

![ER Diagram](diagrams/ERD.png)

---

## Database Normalization

The database is normalized to Third Normal Form (3NF).

### First Normal Form (1NF)

- Atomic values
- No repeating groups

### Second Normal Form (2NF)

- No partial dependencies

### Third Normal Form (3NF)

- No transitive dependencies

---

## Folder Structure

sales-data-warehouse/
│
├── database/
├── datasets/
├── queries/
├── diagrams/
├── dashboard/
├── images/
└── README.md

---

## Features

- Relational database design
- Primary and foreign keys
- Constraints
- Indexes
- Views
- Stored procedures
- Triggers
- Advanced SQL queries
- Business reports

---

## Business Questions Answered

- Top selling products
- Monthly sales revenue
- Revenue by store
- Revenue by country
- Top customers
- Employee performance
- Customer lifetime value
- Inventory status
- Supplier performance
- Product profitability

---

## SQL Concepts Demonstrated

- SELECT
- WHERE
- ORDER BY
- GROUP BY
- HAVING
- INNER JOIN
- LEFT JOIN
- RIGHT JOIN
- Aggregate Functions
- CASE
- Subqueries
- Common Table Expressions (CTEs)
- Window Functions
- Views
- Stored Procedures
- Triggers
- Transactions

---

## Sample Queries

### Top 10 Selling Products

```sql
SELECT
    p.product_name,
    SUM(oi.quantity) AS total_sold
FROM order_items oi
JOIN products p
ON oi.product_id = p.product_id
GROUP BY p.product_name
ORDER BY total_sold DESC
LIMIT 10;
```

### Monthly Revenue

```sql
SELECT
    MONTH(order_date) AS month,
    SUM(quantity * unit_price) AS revenue
FROM orders o
JOIN order_items oi
ON o.order_id = oi.order_id
GROUP BY MONTH(order_date);
```

---

## Screenshots

(Add screenshots here.)

Example:

- ER Diagram
- SQL query results
- Database tables
- Power BI dashboard

---

## Future Improvements

- Customer segmentation
- Sales forecasting
- Inventory prediction
- Data warehouse star schema
- Power BI dashboard enhancements

---

## Skills Demonstrated

- SQL
- Database Design
- Data Modeling
- Normalization
- Business Intelligence
- Data Analysis
- Query Optimization
- Git
- GitHub

---

## Author

**Your Name**

Business Administration and Information Systems Student

Addis Ababa University

LinkedIn:
(Add your LinkedIn URL)

GitHub:
(Add your GitHub URL)
