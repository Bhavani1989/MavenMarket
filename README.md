# Maven Market Power BI Project

## 🧾 Overview

This Power BI report provides a comprehensive analysis of Maven Market's sales, product performance, customer behavior, and return trends across North America using transactional data from 1997–1998.

### Project Stages:
1. **Data Preparation**
2. **Data Modeling**
3. **DAX Calculations**
4. **Interactive Dashboard Design**

---

## 📁 Data Sources

The following CSV files were used:
- `MavenMarket_Customers.csv`
- `MavenMarket_Products.csv`
- `MavenMarket_Stores.csv`
- `MavenMarket_Regions.csv`
- `MavenMarket_Calendar.csv`
- `MavenMarket_Returns.csv`
- `MavenMarket_Transactions_1997.csv`
- `MavenMarket_Transactions_1998.csv`

---

## 🛠️ Data Preparation (Power Query)

Main transformations:
- Promoted headers, corrected data types
- Created new columns:
  - Customers: `full_name`, `birth_year`, `has_children`
  - Products: `discount_price`, `avg_retail_price`
  - Stores: `full_address`, `area_code`
  - Calendar: weekend flag, `month`, `quarter`, `year`
- Null handling: replaced with 0
- Combined transaction files from 1997 & 1998

---

## 🧩 Data Model

**Star Schema** design:
- **Fact Tables**: `Transaction_Data`, `Return_Data`
- **Dimension Tables**: `Customers`, `Products`, `Stores`, `Calendar`, `Regions`
- One-to-many relationships with single-directional filter flow
- Foreign keys hidden in report view

---

## 📊 Key DAX Measures

### 📈 Sales & Profitability
- Quantity Sold
- Total Transactions
- Total Revenue
- Total Profit
- Profit Margin

### 🔁 Returns
- Quantity Returned
- Total Returns
- Return Rate

### 🕒 Time Intelligence
- YTD Revenue
- 60-Day Revenue
- Last Month: Transactions, Revenue, Profit, Returns
- Revenue Target (+5% MoM)
- Weekend KPIs

### 🔍 Other KPIs
- Unique Products
- Brand/Region-based breakdowns

---

## 🧭 Main Dashboard

- KPI Cards (Current Month vs. Targets)
- Brand Matrix (Top 30 Brands: Transactions, Profit, Margin, Return Rate)
- Revenue Trend: Weekly, 1998
- Map & Treemap: Geographic Distribution
- Revenue Gauge
- Country Slicer (USA, Canada, Mexico)
- Bookmark Navigation

---

## 🧪 Product Analysis Dashboard

![Product Analysis Dashboard](ProductAnalysis.png)

This page provides in-depth insights into product-level performance and is accessible via **drill-throughs** from:

- **Product Brand** in the **Main Dashboard**
- **Sales District** in the **Region Analysis Dashboard**

### 🔍 Purpose of Drill-Throughs:
- Analyze **top-performing products** within a specific **brand** or **geographical region**
- Identify **sales drivers**, **profit leaders**, and **return trends** for filtered segments 

### 🧩 Visual Components:
- **Top 20 Products** in the selected brand or district
- **KPI Gauges**: Revenue vs. Target, Profit vs. Target, Sales vs. Target
- **Weekly Sales Line Chart**
- **Transactions by Price Range** (Mid, High, Low)
- **Summary Insight Box**: Narrative summary of the top product’s performance

This drill-through functionality adds context to performance by allowing users to **zoom in on specific contributors** within broader metrics, making the dashboard more actionable and exploratory.


---

## 👥 Customer Analysis Dashboard

- Top 30 Customers by Spend, Quantity, and Transactions
- Purchase Behavior by:
  - Member Card Type
  - Occupation
  - Income Level
- Most Purchased Product per Customer
- Customer Count by Country

---

## 🌍 Region Analysis Dashboard

![Region Analysis Dashboard](RegionAnalysis.png)

This dashboard provides a detailed regional breakdown of sales performance, including trends, returns, and top-performing districts.

### 🧭 Interactive Features

- **Slicer Panel**:
  - **Sales Region Selector** – View data by specific region or all regions combined
  - **Year Selector** – Filter data by year (1997 or 1998)

- **Field Parameters for Metric Selection**:
  - Users can dynamically switch the trend line chart to show:
    - Revenue (default)
    - Profit
    - Total Sales
    - Returns
    - Transactions

This flexibility allows for **customized analysis** based on the business question at hand.

### 📈 Visual Components
- **Sales by District** – Green bar chart
- **Returns by District** – Red funnel chart
- **District-Level Table** – Sold units, returned, revenue, profit, and transactions
- **Revenue Trend (Dynamic)** – Line/area chart that updates based on selected metric
- **Map Visualization** – Active sales districts across North America

This dashboard is optimized for **regional managers and executives**, enabling them to monitor territory-level performance and dig into specific areas of interest using intuitive filters and field selectors.

---

## 🧭 Navigation & Usability

All report pages include **custom page navigation buttons** located in the left pane for easy access across:

- Main Dashboard
- Product Analysis
- Customer Analysis
- Region Analysis

This enables users to move seamlessly between pages, improving user experience and making exploration more intuitive. Bookmarks and drill-throughs are also implemented to allow contextual deep-dives into specific data views.

---

> 🔄 Page includes built-in navigation for seamless transitions across report views.


> 📌 *Note: All insights are based on 1997–1998 data, used for analytical demonstration only.*
