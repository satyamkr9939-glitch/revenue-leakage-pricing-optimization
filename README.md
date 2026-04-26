# 📌 Revenue-Leakage-Analysis-SQL-PowerBI

![Dashboard Overview](dashboard/screenshots/overview.png)

🚀 **End-to-end SQL + Power BI project** analyzing revenue loss in a food delivery platform.

💡 **Impact:** Identified **~10% revenue leakage**, primarily driven by **medium-priced orders** and **high-volume cities**.

---

## 🔗 Links

* 💻 **GitHub Repo:** https://github.com/satyamkr9939-glitch/Revenue-Leakage-Data-Quality-Analysis
* 🔗 **LinkedIn:** https://www.linkedin.com/in/satyam-8b105032b

---

## 🎯 Business Problem

Discount-led growth can hide profitability issues.
This project answers:

* Where is revenue leaking?
* What is driving the leakage?
* Which segments and cities need optimization?

---

## 📊 Key Insights

### 🔴 KPI Snapshot

* **Total Revenue:** 29.85M
* **Revenue Leakage:** 3.32M
* **Leakage Rate:** ~10%

---

### 🌍 City-Level Leakage

![City Analysis](dashboard/screenshots/city_analysis.png)

* Top leakage cities:

  * **Mumbai**
  * **Hyderabad**
  * **Chennai**

👉 Indicates **location-specific pricing inefficiencies**

---

### 💰 Price Segment Driver

![Price Segment](dashboard/screenshots/price_segment.png)

* **Medium-priced orders contribute the highest leakage**
  👉 Shows **misaligned discount strategy in mid-tier pricing**

---

### 🏪 High-Risk Restaurants

![Restaurants](dashboard/screenshots/restaurants.png)

* Small group of restaurants drives majority of losses
  👉 Demonstrates **Pareto effect (80/20 rule)**

---

## ⚙️ Approach

### 1. Data Cleaning (SQL)

* Removed invalid ratings (`NEW`, `-`)
* Standardized price formats
* Handled missing values

### 2. Revenue Modeling

* Estimated expected revenue using reverse pricing logic
* Defined:

  * **Revenue Leakage = Expected – Actual**

### 3. Power BI (DAX + Dashboard)

* Built measures:

  * Total Revenue
  * Expected Revenue
  * Revenue Leakage
  * Leakage %
* Designed interactive visuals for decision-making

---

## 📈 What Makes This Project Strong

* Focus on **business impact**, not just queries
* Uses **derived metrics (expected revenue model)**
* Combines **SQL + DAX + visualization**
* Clear **decision-oriented insights**

---

## 🎯 Recommendations

* Optimize discounts (especially **mid-tier pricing**)
* Monitor **top-loss restaurants**
* Apply **city-specific pricing controls**
* Improve **data validation systems**

---

## 🛠️ Tech Stack

* **SQL** (Data Cleaning, Aggregations, CTEs)
* **Power BI** (DAX, Dashboarding)
* **Excel / CSV**

---

## 📂 Project Structure

```id="d1h8al"
revenue-leakage-pricing-optimization/
│
├── data/
├── sql/
│   ├── 01_data_cleaning.sql
│   ├── 02_revenue_analysis.sql
│   ├── 03_leakage_analysis.sql
│
├── dashboard/
│   ├── powerbi.pbix
│   └── screenshots/
│       ├── overview.png
│       ├── city_analysis.png
│       ├── price_segment.png
│       ├── restaurants.png
│
└── README.md
```

---

## 🚀 Skills Demonstrated

* Data Cleaning & Validation
* Business Analytics & Insight Generation
* SQL (CTE, Aggregations)
* DAX & Data Modeling
* Dashboard Design & Storytelling

---

## 💡 Note

This project simulates a **real-world analytics scenario** focused on **pricing optimization and profitability improvement**.

---

## 🤝 Connect

* LinkedIn: https://www.linkedin.com/in/satyam-8b105032b
* GitHub: https://github.com/satyamkr9939-glitch
