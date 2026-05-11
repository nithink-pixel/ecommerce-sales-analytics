# 🛒 E-Commerce Sales Performance Analytics

**Author:** Nithin Krishna | M.S. Business Analytics | UMass Isenberg  
**Tools:** Python · SQL · Tableau · Pandas · Statsmodels · Seaborn  
**Dataset:** Brazilian E-Commerce Public Dataset (Olist) — 100,000+ real orders (2016–2018)  

---

## 📌 Business Problem

Every e-commerce business has the same core questions:
- Which products and regions drive the most revenue?
- What factors lead to higher customer satisfaction?
- Which customers are most valuable and how do we retain them?
- Can we predict revenue using operational metrics?

This project answers all four using real Brazilian e-commerce data across 100,000+ orders, 30,000+ products, and 3,000+ sellers.

---

## 📊 Key Findings

| Metric | Value |
|---|---|
| Total Orders Analyzed | 96,478 delivered orders |
| Avg Order Value | R$ 140.32 |
| On-Time Delivery Rate | 92.1% |
| Avg Review Score | 4.09 / 5.0 |
| OLS R-squared | 0.67 |

**Top Insights:**
- Health & Beauty and Computers & Accessories are the top revenue categories
- Fast delivery (≤7 days) generates review scores 0.8 points higher than slow delivery
- OLS regression shows product price explains 67% of revenue variance
- São Paulo drives 42% of total revenue
- Champions segment represents 8% of customers but 34% of revenue

---

## 🔍 Analysis Structure

### 1. Data Cleaning & Merging
- Merged 7 relational tables into one analytical dataset
- Engineered features: delivery delay days, on-time flag, revenue per order
- Removed outliers: delivery over 120 days, revenue at or below 0
- Final clean dataset: 96,478 records

### 2. Visualizations (7 Charts)
- Monthly revenue trend with 3-month rolling average
- Top 10 product categories by total revenue
- Review score distribution by delivery speed (boxplot)
- Correlation heatmap of key business metrics
- Revenue and avg order value by state
- OLS actual vs predicted revenue
- RFM customer segment distribution

### 3. OLS Regression — Revenue Drivers
