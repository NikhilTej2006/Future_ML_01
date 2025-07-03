# 📈 Retail Sales Forecasting Dashboard

An end-to-end machine learning and business intelligence solution that forecasts retail sales using historical data and presents results via an interactive Power BI dashboard. This project demonstrates how AI/ML can assist retail companies in planning, budgeting, and making data-driven decisions.

---
## 📦 Dataset

**Source**: [Tevec Systems – Retail Sales Forecasting Dataset (Kaggle)](https://www.kaggle.com/datasets/tevecsystems/retail-sales-forecasting)  
**Fields**:
- `data`: Date of transaction
- `venda`: Units sold
- `estoque`: Inventory stock level
- `preco`: Product price

---

## 🧰 Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Python (Jupyter Notebook)** | Data cleaning, EDA, feature engineering, and forecasting |
| **Facebook Prophet** | Time series sales forecasting |
| **Pandas, NumPy, Matplotlib, Seaborn** | Data wrangling and visualization |
| **Power BI Desktop** | Dashboard creation and interactivity |
---

## 🔁 Project Workflow

1. **Data Preprocessing**
   - Checked for nulls, data types, and duplicates
   - Parsed and sorted date column
   - Created new columns: `Month`, `Year`, `MonthYear`, `Weekday`

2. **Exploratory Data Analysis (EDA)**
   - Trend analysis and seasonality checks
   - Rolling statistics, moving averages
   - Lag features to capture prior day/week/month behavior

3. **Forecasting Model**
   - Trained Prophet on `venda` with `data` as `ds`
   - Included yearly and weekly seasonality
   - Generated 30-day forecast with upper/lower confidence intervals

4. **Interactive Dashboard**
   - Power BI dashboard featuring:
     - Actual vs Forecast line chart
     - Monthly & weekday sales trends
     - KPI cards for quick insights
     - Date slicers and filters
     - Text-based business recommendations

## 🔍 Key Insights

- 📈 **Sales show strong monthly trends**, with spikes in March and November.
- 🛍️ **Weekends and start-of-month periods consistently outperform weekdays**.
- 📉 **February is a low-performing month**, suggesting potential for targeted marketing or discounts.
- 📊 **Prophet forecast indicates an expected 8–12% growth over the next 30 days**.
- 📦 Inventory and sales show moderate correlation — suggesting supply-demand balance is critical.

---


## 📂 Folder Structure

```bash
Retail-Sales-Forecasting/
├── data/
│   └── tevec_retail_sales.csv
├── forecast_output.csv
├── prophet_forecast.ipynb
├── RetailDashboard.pbix
├── dashboard-export.pdf
└── README.md
