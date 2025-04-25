# Revenue-Analysis-Dashboard

A Power BI dashboard project analyzing coffee sales data sourced from Kaggle. The goal is to provide actionable business insights through KPIs, product and regional performance analysis, and time series trends.

---

## 📁 Dataset Overview

The dataset contains coffee sales transactions with the following key columns:

- `transaction_id`
- `transaction_date`
- `transaction_qty`
- `store_id`
- `store_location`
- `product_id`
- `unit_price`
- `product_category`
- `product_type`
- `product_detail`

---

## 🧹 Data Cleaning (Power Query)

- Removed duplicate records and null values
- Standardized column names
- Converted data types:
  - Dates → Date type
  - Quantities and Prices → Numeric
- Created new column:
  - `revenue = transaction_qty * unit_price`

---

## 🧠 DAX Measures

| KPI / Metric             | DAX Expression |
|--------------------------|----------------|
| Total Sales              | `SUM(revenue)` |
| Average Order Value      | `[Total Sales] / DISTINCTCOUNT(transaction_id)` |
| Total Quantity Sold      | `SUM(transaction_qty)` |

---

## 📊 Dashboard Features

### 🎯 KPIs (Card Visuals)
- Total Sales Revenue
- Average Order Value
- Total Quantity Sold

### 🛒 Product Analysis
- Top Products by Volume and Revenue (Table visuals)

### 📈 Time Series Analysis
- Line chart showing sales trends over time (monthly)
## 📌 Insights Generated

- Identified top-selling coffee products and their revenue contribution
- Evaluated underperforming product categories
- Tracked seasonal trends in coffee sales
- Visualized store-wise performance for geographic strategy
- 
## ⭐️ Star this repo if you like the project!
