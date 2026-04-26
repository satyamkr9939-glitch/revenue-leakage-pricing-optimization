# 🧾 SQL Analysis — Revenue Leakage Project

This folder contains all SQL scripts used for **data cleaning, validation, and revenue leakage analysis**.

---

## 📂 Files Overview

* **01_data_cleaning.sql** → Data preprocessing and cleaning
* **02_revenue_analysis.sql** → Core revenue metrics and aggregation
* **03_leakage_analysis.sql** → Revenue leakage modeling and insights

---

## 🧹 1. Data Cleaning

Key operations performed:

* Removed invalid values (`NEW`, `-`) from ratings
* Converted price column to numeric format
* Handled missing and null values
* Standardized column names

👉 Goal: Ensure **data consistency and reliability**

---

## 📊 2. Revenue Analysis

Calculated key business metrics:

* Total Revenue
* Average Order Value
* Orders per City

### Example Query:

```sql id="u7h8c2"
SELECT 
    City,
    COUNT(*) AS total_orders,
    SUM(price_cleaned) AS total_revenue,
    AVG(price_cleaned) AS avg_order_value
FROM clean_data
GROUP BY City;
```

👉 Insight: Identifies **top-performing cities**

---

## 💣 3. Revenue Leakage Analysis

Since discount data was not available, revenue leakage was estimated using **reverse pricing logic**.

### Formula:

```id="s8c3tp"
Expected Price = Actual Price / 0.9
Leakage = Expected - Actual
```

---

### Example Query:

```sql id="4kq9pf"
WITH revenue_calc AS (
    SELECT 
        City,
        price_cleaned AS actual_price,
        price_cleaned / 0.9 AS expected_price,
        (price_cleaned / 0.9) - price_cleaned AS leakage
    FROM clean_data
)
SELECT 
    City,
    SUM(leakage) AS total_leakage
FROM revenue_calc
GROUP BY City
ORDER BY total_leakage DESC;
```

👉 Insight: Identifies **high-loss cities**

---

## 🏪 4. Restaurant-Level Analysis

```sql id="r2z6xm"
SELECT 
    Place_Name,
    COUNT(*) AS total_orders,
    SUM((price_cleaned / 0.9) - price_cleaned) AS total_leakage
FROM clean_data
GROUP BY Place_Name
ORDER BY total_leakage DESC
LIMIT 10;
```

👉 Insight: Finds **top loss-making restaurants**

---

## 🚀 5. Advanced SQL Techniques Used

* Common Table Expressions (CTEs)
* Aggregations (SUM, AVG, COUNT)
* CASE statements for segmentation
* Window functions (RANK)

---

## 🎯 Key Outcome

SQL analysis revealed:

* ~10% estimated revenue leakage
* High leakage concentrated in specific cities and restaurants
* Medium-priced orders contribute significantly to losses

---

## 💡 Note

This analysis simulates a real-world scenario where direct discount data is unavailable, requiring **derived metrics and assumptions**.

---
