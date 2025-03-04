# Pizza-Sales-Management-System-SQL-


## 📌 Project Overview
The **Pizza Sales Management System** is a SQL-based project designed to analyze and optimize pizza sales, track revenue, and improve inventory management. Using structured **SQL queries**, this project provides key business insights to enhance decision-making.

## 🚀 Key Features
- **Total Orders & Revenue Analysis**: Extract total orders placed and identify the highest revenue-generating pizza.
- **Sales Trends & Customer Preferences**: Determine peak sales hours, best-selling pizza types, and customer demand patterns.
- **Inventory Optimization**: Forecast stock levels based on sales performance.

## 🛠 Technologies Used
- **Database**: SQL (MySQL / PostgreSQL / SQLite)
- **Techniques**: Joins, Aggregations, Subqueries, Case Statements
- **Tools**: SQL Queries for Data Analysis

## 📊 SQL Queries Used
### 1️⃣ Retrieve Total Orders Placed
```sql
SELECT COUNT(*) AS TotalOrders FROM orders;
```
### 2️⃣ Find the Highest Revenue-Generating Pizza
```sql
SELECT PizzaID, SUM(Quantity * Price) AS TotalRevenue 
FROM orders JOIN pizzas USING(PizzaID)
GROUP BY PizzaID ORDER BY TotalRevenue DESC LIMIT 1;
```
### 3️⃣ List the Top 5 Best-Selling Pizzas
```sql
SELECT PizzaID, COUNT(*) AS TotalOrders 
FROM orders GROUP BY PizzaID ORDER BY TotalOrders DESC LIMIT 5;
```

## 📌 Business Insights
✔ **Most Ordered Pizzas** – Helps focus marketing efforts on popular items.  
✔ **Peak Sales Hours** – Identify high-demand times for better staffing and promotions.  
✔ **Revenue Trends** – Understand sales performance for strategic decision-making.  
✔ **Inventory Planning** – Optimize stock levels based on demand.





