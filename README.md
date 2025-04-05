# 📦 Inventory Optimization (SQL in Google Colab)

This project demonstrates how to analyze and optimize inventory using SQL queries in a Google Colab environment with SQLite. It’s a beginner-friendly project that simulates a small retail inventory dataset and helps identify key business actions.

---

## 🧰 Tools Used

- **Google Colab** (no installation needed)
- **SQLite** (via Python's `sqlite3`)
- **Pandas** for data handling

---

## 📊 Problem Statement

The goal is to optimize stock levels by identifying:
- Products that are **below reorder level**
- **Total units sold** by product category
- **Reorder suggestions** based on current stock vs. reorder level

---

## 📁 Dataset (Simulated)

The dataset includes fields like:

- `Product_ID`
- `Product_Name`
- `Category`
- `Units_Sold`
- `Current_Stock`
- `Reorder_Level`

---

## 🔍 SQL Queries Performed

1. **Low Stock Products**

   SELECT Product_Name, Current_Stock, Reorder_Level
   FROM inventory
   WHERE Current_Stock < Reorder_Level

2. **Total Sales by Category**

SELECT Category, SUM(Units_Sold) AS Total_Sales
FROM inventory
GROUP BY Category


3. **Reorder Suggestions**

SELECT Product_Name, (Reorder_Level - Current_Stock) AS Units_To_Order
FROM inventory
WHERE Current_Stock < Reorder_Level


🚀 How to Use
Open the Colab notebook: Inventory_Optimization_with_SQL.ipynb

Run all cells from top to bottom

Modify data or queries as needed to explore
