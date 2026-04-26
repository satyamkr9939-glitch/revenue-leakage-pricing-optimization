# 📊 Power BI Dashboard — Revenue Leakage Analysis

This folder contains the **Power BI dashboard (.pbix)** and supporting screenshots used to analyze revenue leakage.

---

## 📁 Files

* **powerbi.pbix** → Main dashboard file
* **screenshots/** → <img width="1311" height="728" alt="Screenshot 2026-04-26 115813" src="https://github.com/user-attachments/assets/e7cbb5df-d294-4b30-afcc-56288695d9bb" />


---

## 🎯 Dashboard Objective

To provide a **clear, interactive view of revenue leakage** and help stakeholders:

* Identify where revenue is being lost
* Understand key drivers of leakage
* Make data-driven pricing decisions

---

## 📸 Dashboard Preview

![Overview](screenshots/overview.png)

---

## 📊 Key Metrics (DAX Measures)

### 🔢 Total Revenue

```DAX id="k3s91a"
Total Revenue = SUM('zomato_Dataset'[Prices])
```

---

### 🔢 Expected Revenue

```DAX id="h92kpl"
Expected Revenue =
SUMX(
    'zomato_Dataset',
    'zomato_Dataset'[Prices] / 0.9
)
```

---

### 🔢 Revenue Leakage

```DAX id="z7nq4r"
Revenue Leakage =
[Expected Revenue] - [Total Revenue]
```

---

### 🔢 Leakage %

```DAX id="v4t8xp"
Leakage % =
DIVIDE([Revenue Leakage], [Expected Revenue])
```

---

## 📈 Dashboard Visuals

### 🔴 KPI Cards

* Total Revenue
* Revenue Leakage
* Leakage %

👉 Provides quick summary of business performance

---

### 🌍 Revenue Leakage by City

![City](screenshots/city_analysis.png)

* Highlights cities with highest revenue loss
* Helps identify regional inefficiencies

---

### 💰 Revenue Leakage by Price Segment

![Segment](screenshots/price_segment.png)

* Shows that **medium-priced orders drive maximum leakage**

---

### 🏪 Top Risk Restaurants

![Restaurants](screenshots/restaurants.png)

* Identifies restaurants contributing most to losses

---

## 🎛️ Interactivity

* Filters:

  * City
  * Price Segment

👉 Enables dynamic analysis and exploration

---

## 🎨 Design Principles

* Clean and minimal layout
* Red color used to highlight leakage (problem area)
* Consistent formatting across visuals
* Insight-driven titles for better storytelling

---

## 🎯 Key Insight

> ~10% revenue leakage observed, primarily driven by medium-priced orders and high-volume cities.

---

## 🚀 Business Value

* Helps optimize pricing strategy
* Identifies high-risk areas for intervention
* Supports data-driven decision-making

---

## 💡 Note

This dashboard is designed with a focus on **business storytelling**, not just visualization.

---
