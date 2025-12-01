<h1 align="center" style="font-weight:700;">
  🌾 India Multi-Crop Production & Yield Analysis Dashboard
</h1>

<h3 align="center" style="color:#555;">
  (1966–2017)
</h3>

<p align="center">
  <img src="https://img.icons8.com/color/48/power-bi.png" width="45" alt="Power BI"/>
  <img src="https://www.citypng.com/public/uploads/preview/hd-python-logo-symbol-transparent-png-735811696257415dbkifcuokn.png" width="45" alt="Python"/>
  <img src="https://img.icons8.com/color/48/csv.png" width="45" alt="CSV"/>
  <img src="https://www.vhv.rs/dpng/d/478-4788452_vector-db-symbol-sql-azure-hd-png-download.png" width="45" alt="Database"/>
  <img src="https://cdn-icons-png.flaticon.com/512/9755/9755793.png" width="45" alt="Markdown"/>
</p>

<p align="center" style="color:#444; font-size:16px;">
  A Power BI Mini Project for Multi-Crop Agricultural Analytics  
</p>

---
## 📌 Overview
This project analyzes India’s multi-crop agricultural performance over 52 years (1966–2017) using an interactive Power BI dashboard.  
It highlights trends in area, production, yield, states' performance, and long-term growth.

---

## 🎯 Objectives
- Analyze area, production, and yield across multiple crops.
- Understand state-wise and district-wise performance.
- Evaluate long-term and 5-year growth trends.
- Identify high-performing and low-performing regions.
- Build an interactive, corporate-style Power BI dashboard.

---

## 📂 Dataset Description
The dataset (**Agri_Data.csv**) includes:

### General Columns
- Year  
- State Name  
- Dist Name  

### Crop Area/Production/Yield Columns (Examples)
- 🌾 Rice → AREA, PRODUCTION, YIELD  
- 🌾 Wheat → AREA, PRODUCTION, YIELD
- 🌽 Maize → AREA, PRODUCTION, YIELD
- 🌾 Sorghum (Kharif & Rabi)  
- 🌱 Soyabean  
- 🧵 Cotton  
- 🌴 Sugarcane  
- 🌱 Oilseeds  
- 🌻 Sunflower  

### Dataset Coverage
- 50+ years  
- 18+ crops  
- All major states  
- Multiple districts per state  

---

## 📊 Dashboard Features

### 1️⃣ Executive Summary
- KPIs  
- India map for production distribution  
- Yearly trend of major crops  

### 2️⃣ Crop Performance Analysis
- Line & Clustered Column Chart (Area vs Yield)
- Crop Efficiency Funnels  
- Stacked Yield Comparison by State

### 3️⃣ State & District Insights
- State-level long-term crop trends  
- District-level summarization & ranking  

### 4️⃣ Growth & Trend Analytics
- 5-year growth calculations  
- Scatter chart (Growth % vs Total Production)
- Top/Bottom performing regions  

---

## 🧮 Key DAX Measures

### Total Production
```
Total Production =
SUM('agri_data'[RICE PRODUCTION (1000 tons)]) +
SUM('agri_data'[WHEAT PRODUCTION (1000 tons)]) +
SUM('agri_data'[MAIZE PRODUCTION (1000 tons)])
```

### 5-Year Growth %
```
5-Year Growth % =
VAR CurrentProd = [Total Production]
VAR Prod5YearsAgo =
    CALCULATE(
        [Total Production],
        FILTER(ALL('DimDate'[Year]), 'DimDate'[Year] = MAX('DimDate'[Year]) - 5)
    )
RETURN DIVIDE(CurrentProd - Prod5YearsAgo, Prod5YearsAgo)
```

---

## 🛠 Power Query Steps
- Remove duplicates  
- Clean State/District names  
- Convert Year → Whole Number  
- Replace null numerical values with 0  
- Data type correction for all columns  
- Unpivot yield columns for stacked visuals  

---

## 📁 Project Structure
```
📦 Multi-Crop Analysis Project
 ┣ 📊 agri_powerbi.pbix
 ┣ 📝 README.md
 ┣ 📘 agri.ipynb
 ┣ 🛢️ agri_sql_queries.sql
 ┣ 📋 agri_data.csv
 ┗ 📁 EDA Charts
    ┗ 🖼️ images

```

---

## 🔍 Key Insights
- Rice & Wheat dominate agricultural output.
- Cotton & Soybean show major growth post-2000.
- Several states show high area but low yield.
- Green Revolution years show sharp increases in production.
- Scatter analysis identifies high production but low growth states.

---

## 💼 Tools Used
- Power BI Desktop  
- DAX  
- Power Query  
- Python  
- CSV dataset (agri_data)  

---

## 📘 Conclusion
This project provides a detailed agricultural performance evaluation across 50+ years.  
It demonstrates the power of Business Intelligence (BI) tools for real-world analytics and decision-making.

---

## 👤 Author
**Girija**  
Power BI Mini Project | 2025  

