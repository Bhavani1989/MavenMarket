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
  
![Image](https://github.com/user-attachments/assets/2c5bf4c4-bfba-490c-a550-60d22215bd70)
---

## 🧪 Product Analysis Dashboard

This page provides in-depth insights into product-level performance and is accessible via **drill-throughs** from:

- **Product Brand** in the **Main Dashboard**
- **Sales District** in the **Region Analysis Dashboard**

### 🔍 Purpose of Drill-Throughs:
- Analyze **top-performing products** within a specific **brand** or **geographical region**
- Identify key contributors to revenue, profit, and returns
- Understand product performance in specific contexts

### 🧰 Custom Tooltip Feature
A custom-designed **product tooltip** is enabled on this page:
- **Pops up when hovering over any product**
- Displays detailed metrics:
  - Product Name
  - Revenue
  - Units Sold
  - Profit
  - Returns
  - Return Rate
  - **Mini Sales Trend Chart**

    ![Image](https://github.com/user-attachments/assets/7915c4b0-4120-4da1-8d6e-e70f816e8c18)
    

This tooltip allows users to **quickly assess product performance at a glance** without leaving the current visual context.

### 🧩 Visual Components:
- **Top 20 Products** in the selected brand or district
- **KPI Gauges**: Revenue vs. Target, Profit vs. Target, Sales vs. Target
- **Weekly Sales Line Chart**
- **Transactions by Price Range** (Mid, High, Low)
- **Summary Insight Box**: Narrative summary of the top product’s performance

This drill-through functionality adds context to performance by allowing users to **zoom in on specific contributors** within broader metrics, making the dashboard more actionable and exploratory.

![Image](https://github.com/user-attachments/assets/d3a5c21c-8cf7-4550-b75e-479d6287b0ff)

---

## 👥 Customer Analysis Dashboard

- Top 30 Customers by Spend, Quantity, and Transactions
- Purchase Behavior by:
  - Member Card Type
  - Occupation
  - Income Level
- Most Purchased Product per Customer
- Customer Count by Country
  
 ![Image](https://github.com/user-attachments/assets/666f1016-5ff5-44fe-9ac4-c75888ff2568)
 
---

## 🌍 Region Analysis Dashboard

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

![Image](https://github.com/user-attachments/assets/9017e2e0-188d-447c-8f08-b1f59516c1a1)

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


## 📌 Notes

- This model uses synthetic data and is ideal for **learning**, **training**, and **demo** purposes.
- It demonstrates core **data modeling**, **DAX calculations**, and **dashboarding** skills used in business analytics.

---

## 📝 Future Enhancements

- Add **forecasting models** using Power BI built-in forecasting or Python integration.
- Include **RLS (Row-Level Security)** for multi-user reporting environments.
- Integrate **external benchmarking datasets** for comparative analysis.
- Deploy the report to Power BI Service for automated refresh and sharing.

---
## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## 🙌 Acknowledgments

- Maven Analytics Learning & Development team
- Power BI Community for DAX and visualization best practices

---
