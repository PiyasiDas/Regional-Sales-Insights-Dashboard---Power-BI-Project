# 📊 Regional Sales Insights Dashboard | Power BI Project

This project presents a dynamic **Power BI dashboard** that delivers actionable insights into sales performance across different regions. It helps businesses monitor KPIs, identify regional trends, analyze customer segments, and forecast future sales — all in one interactive visualization tool.

---

## 🚀 Project Objective

To create a **regional-level sales insights dashboard** using Power BI that enables business stakeholders to:

- Track performance across different regions
- Analyze category-wise and segment-wise sales patterns
- Understand key KPIs such as Total Sales, Profit, Quantity, and Avg. Delivery Time
- Predict upcoming sales trends using a 30-day rolling forecast

---

## 🧰 Tools & Technologies Used

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Power Query Editor**
- **Excel / CSV (Data Source)**
- **Map Visualization** (ArcGIS or Built-in Power BI Map)

---

## 📈 Key Metrics and Features

### ✅ KPIs:
- **Total Sales**: 2M+
- **Quantity Sold**: 22K+
- **Total Profit**: 175K+
- **Average Delivery Time**: 4 days

### ✅ Visuals:
- Pie Charts: Sales by Region, Segment, and Payment Mode
- Line & Area Charts: Monthly Sales and Profit (Year-over-Year)
- Bar Charts: Sales by Category, Sub-Category, Ship Mode, and State
- Map Visualization: Sales & Profit by U.S. State
- Forecast Line Charts: 30-Day Sales Predictions

---

## 📊 DAX Measures Used

```DAX
-- 1. Average Delivery Time
AvgDeliveryTime = AVERAGE(Sales_Dataset[DeliveryTime])

-- 2. Sales Forecast Table
SalesForecast = 
    SUMMARIZE(
        Sales_Dataset,
        Sales_Dataset[Order Date],
        "Total_Sales", SUM(Sales_Dataset[Sales])
    )
