# Grocery Product Analysis Dashboard

## 📌 Project Overview

The **Grocery Product Analysis Dashboard** is a Power BI business analytics project designed to help a grocery business understand its **product-line performance, sales volume, pricing, and product-level demand**.

The dashboard transforms supermarket transaction data into interactive KPIs and visual insights that can support **product management, sales monitoring, and business decision-making**.

---

## 💼 Business Case

A grocery business sells products across multiple product lines, but simply having transaction data does not clearly show which product categories are contributing to sales volume or how pricing and quantity vary across product lines.

The business needs a simple analytical solution to answer questions such as:

* How many different product lines are being sold?
* How many units have been sold in total?
* What is the overall sales value?
* What is the average unit price?
* How much quantity is sold on average per product line?
* Which product lines require greater attention from the business?

The **Grocery Product Analysis Dashboard** addresses these questions by converting raw supermarket sales data into a structured Power BI dashboard.

---

## 🎯 Business Objectives

1. **Monitor overall sales performance**
2. **Measure total product quantity sold**
3. **Understand product-line coverage**
4. **Analyze average unit pricing**
5. **Compare product-line demand**
6. **Support product and sales decisions using data**

---

## 📊 Key Performance Indicators (KPIs)

| KPI                                   | Business Meaning                                        |
| ------------------------------------- | ------------------------------------------------------- |
| **Total Product Lines**               | Number of unique product categories/product lines       |
| **Total Quantity Sold**               | Total number of units sold                              |
| **Total Sales**                       | Total sales value calculated from unit price × quantity |
| **Average Unit Price**                | Average selling price per unit                          |
| **Average Quantity per Product Line** | Average quantity sold for each product line             |

---

## 🧮 DAX Calculations

### 1. Total Product Lines

```DAX
Total Product Lines =
DISTINCTCOUNT('Supermarket Sales 2'[Product line])
```

### 2. Total Quantity Sold

```DAX
Total Quantity Sold =
SUM('Supermarket Sales 2'[Quantity])
```

### 3. Total Sales

```DAX
Total Sales =
SUMX(
    'Supermarket Sales 2',
    'Supermarket Sales 2'[Unit price] *
    'Supermarket Sales 2'[Quantity]
)
```

### 4. Average Unit Price

```DAX
Average Unit Price =
AVERAGE('Supermarket Sales 2'[Unit price])
```

### 5. Average Quantity per Product Line

```DAX
Average Quantity per Product Line =
DIVIDE([Total Quantity Sold], [Total Product Lines])
```

---

## 🔍 Analytical Approach

The project follows a simple business-analysis flow:

**Raw Supermarket Data → Data Preparation → DAX Measures → KPI Analysis → Product Analysis → Business Insights → Recommendations**

The analysis focuses on understanding **what the data shows**, identifying meaningful patterns, and using those findings to support business decisions.

---

## 🛠️ Tools & Technologies

* **Power BI** — Dashboard development and visualization
* **DAX** — KPI and analytical measure calculations
* **Microsoft Excel / CSV** — Data source and data handling
* **Power BI Data Model** — Data analysis and reporting

---

## 📁 Project Files

| File                                | Description                                            |
| ----------------------------------- | ------------------------------------------------------ |
| `.gitignore`                        | Git configuration for excluding unnecessary files      |
| `DAX_Calculations.docx`             | DAX measures used in the project                       |
| `Executive_Sales_Dashboard.png`     | Screenshot of the executive dashboard                  |
| `GPAD1.pbix`                        | Power BI dashboard/project file                        |
| `Recommendation_Justification.docx` | Business recommendations and their supporting analysis |
| `Supermarket Sales 2.csv`           | Supermarket sales dataset used for analysis            |

---

## 📈 Business Value

The dashboard provides a centralized view of supermarket product performance and helps business users move from **raw transaction data to actionable information**.

It can help management:

* Monitor sales and quantity performance
* Understand the product portfolio
* Evaluate pricing patterns
* Identify differences in product-line demand
* Use quantitative evidence when reviewing product performance

---

## 👤 Target Users

This dashboard can be useful for:

* **Business Managers**
* **Sales Managers**
* **Product Managers**
* **Retail Analysts**
* **Data Analysts**

---

## 📌 Project Outcome

The project demonstrates how **Power BI and DAX can be used to convert supermarket transaction data into a business-focused analytical dashboard**.

Rather than focusing only on visualization, the project connects **KPIs → analysis → business insights → recommendations**, demonstrating a practical approach to data-driven decision-making.
