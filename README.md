# 📊 Revenue Leakage Analysis (SQL + Power BI)

![Dashboard Overview] <img width="1311" height="728" alt="Screenshot 2026-04-26 115813" src="https://github.com/user-attachments/assets/a2a8aa82-2f1b-43f3-a0c2-9208b9d20cdc" />


🚀 Identified **~10% revenue leakage** in a food delivery platform using SQL & Power BI
💡 Discovered **medium-priced orders** and **high-volume cities** as primary drivers of revenue loss

---

## 💣 Why This Matters

In discount-driven platforms, poor pricing strategies can silently reduce profitability.
Even a **5–15% revenue leakage** can significantly impact business margins.

👉 This project identifies **where revenue is leaking and why**, enabling data-driven pricing decisions.

---

## 🎯 Business Objective

* Detect revenue leakage
* Identify key drivers (city, price segment, restaurant)
* Provide actionable recommendations

---

## 📊 Key Insights

### 🔴 KPI Snapshot

* **Total Revenue:** 29.85M
* **Revenue Leakage:** 3.32M
* **Leakage Rate:** ~10%

---

### 🌍 City-Level Leakage

![City Analysis] <img width="723" height="572" alt="image" src="https://github.com/user-attachments/assets/df1059ca-78da-45e6-8420-4397119c74fc" />


* Highest leakage in:

  * **Mumbai**
  * **Hyderabad**
  * **Chennai**

👉 Indicates **location-specific pricing inefficiencies**

---

### 💰 Price Segment Analysis

![Price Segment] <img width="896" height="557" alt="image" src="https://github.com/user-attachments/assets/92c891b0-a969-4b45-a0c3-74a9e6e155b8" />


* **Medium-priced orders contribute the highest leakage**

👉 Suggests **misaligned discount strategy in mid-tier pricing**

---

### 🏪 High-Risk Restaurants

![Restaurants] <img width="312" height="268" alt="image" src="https://github.com/user-attachments/assets/2f2ec3f2-7c87-4bba-8940-673bc9b05616" />


* A small group of restaurants drives the majority of revenue loss

👉 Demonstrates **Pareto effect (80/20 rule)**

---

## 🧠 My Approach

1. Cleaned raw dataset (handled missing and invalid values)
2. Standardized price and rating formats
3. Modeled expected revenue using reverse pricing logic
4. Calculated revenue leakage (Expected – Actual)
5. Built interactive Power BI dashboard for insights

---

## ⚙️ Workflow

```
Raw Data → SQL Cleaning → Analysis → Power BI Dashboard → Insights
```

---

## 🧾 Key SQL Concepts Used

* Common Table Expressions (CTEs)
* Aggregations (SUM, AVG, COUNT)
* Data cleaning techniques
* Business metric calculations

---

## 📊 DAX Measures

```DAX id="lqz4hb"
Total Revenue = SUM('zomato_Dataset'[Prices])
```

```DAX id="2r8nqf"
Expected Revenue =
SUMX('zomato_Dataset', 'zomato_Dataset'[Prices] / 0.9)
```

```DAX id="w0lqj3"
Revenue Leakage =
[Expected Revenue] - [Total Revenue]
```

```DAX id="k5g1vd"
Leakage % =
DIVIDE([Revenue Leakage], [Expected Revenue])
```

---

## 🎯 Business Recommendations

* Optimize discount strategy (especially mid-tier pricing)
* Monitor high-risk restaurants
* Apply city-level pricing strategies
* Improve data validation systems

---

## 🛠️ Tech Stack

* SQL
* Power BI (DAX, Visualization)
* Excel / CSV

---

## 📂 Project Structure

```
revenue-leakage-pricing-optimization/
│
├── data/
├── sql/
├── dashboard/
│   ├── powerbi.pbix
│   └── screenshots/
├── docs/
├── README.md
```

---

## 🚀 What Makes This Project Strong

* Focuses on **business impact**, not just analysis
* Uses **derived revenue modeling**
* Combines SQL + DAX + visualization
* Provides **actionable insights**

---

## 💡 One-Line Summary

👉 Built a business-focused analytics solution to detect revenue leakage and support pricing optimization decisions.

---

## 🔗 Connect

* LinkedIn: https://www.linkedin.com/in/satyam-8b105032b
* GitHub: https://github.com/satyamkr9939-glitch

---

