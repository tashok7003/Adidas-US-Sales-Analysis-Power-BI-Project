---

# 📊 Adidas US Sales Analysis – Power BI Project

This repository contains a complete **Power BI data analytics project** built using the **Adidas US Sales Dataset**. The goal of this project is to provide deep insights into sales performance, product trends, retailer contribution, and regional distribution using interactive dashboards.

---

## 📁 Project Structure

```
📂 PowerBI-Adidas-Report
├── adidas_project.pbix                 # Main Power BI report file
├── Adidas US Sales Datasets.xlsx       # Raw dataset used for the report
└── README.md                           # Documentation
```

---

## 📝 Project Overview

The **Adidas US Sales Analysis** project identifies patterns in sales performance across different regions, product categories, retailers, and time periods.
This dashboard is designed to help business teams quickly evaluate KPIs, optimize strategy, and make data-driven decisions.

---

## 🎯 Objectives

* Analyze total sales, profit, units sold, and margin% across the US.
* Identify **best-performing cities, states, products, and retailers**.
* Track **year-over-year (YoY)** and **month-over-month (MoM)** performance.
* Visualize product demand and seasonal trends.
* Build an **interactive Power BI dashboard** for easy exploration.

---

## 📂 Dataset Description

The project uses:

**File:** `Adidas US Sales Datasets.xlsx`
This dataset contains columns such as:

* Date
* Retailer
* Region & State
* City
* Product Category
* Sales Method (Online / In-store)
* Units Sold
* Price per Unit
* Total Sales
* Operating Profit
* Operating Margin

---

## 🛠 Tools & Technologies Used

| Tool / Tech          | Purpose                                           |
| -------------------- | ------------------------------------------------- |
| **Power BI Desktop** | Data Cleaning, Modeling & Dashboard Visualization |
| **Excel**            | Raw dataset storage & basic preprocessing         |
| **DAX**              | Measures & calculated columns                     |
| **Power Query**      | Data transformations                              |

---

## 📐 Data Modeling

The report uses **cleaned and transformed tabular data** modeled using:

* Dimensional modeling
* Date table with calendar columns
* Relationships based on retailer, region, and product attributes
* DAX measures (e.g. Total Sales, Profit %, YoY growth)

> The `.pbix` file includes all model relationships and measures.

---

## 📊 Dashboard Features

### ✔ KPIs

* Total Sales
* Total Profit
* Units Sold
* Operating Margin
* YoY & MoM Growth

### ✔ Visual Insights

* **Sales by Region** – Map & bar charts
* **Sales by Retailer**
* **Top Products**
* **Sales Trend Over Time**
* **Profitability Analysis**
* **Sales Method Breakdown** (Online vs Offline)

### ✔ Filters/Slicers

* Year
* Region
* Retailer
* Product Category
* Sales Method

---

## ▶ How to Use the Report

1. Download the `.pbix` file from the repository
2. Open it using **Power BI Desktop**
3. Interact with slicers and visuals to explore insights

---

## 🧮 DAX Measures (Highlighted Examples)

```DAX
Total Sales = SUM('Adidas'[Total Sales])

Total Profit = SUM('Adidas'[Operating Profit])

Operating Margin % = DIVIDE([Total Profit], [Total Sales], 0)

YoY Sales Growth = 
VAR PreviousYear =
    CALCULATE([Total Sales], SAMEPERIODLASTYEAR('Date'[Date]))
RETURN DIVIDE([Total Sales] - PreviousYear, PreviousYear)
```

## 🚀 Future Improvements

* Automate dataset refresh using Power BI Service
* Add forecasting using Power BI AI visuals
* Incorporate external datasets (e.g., US population, inflation)
* Build a paginated report for PDF export

  ---

---
