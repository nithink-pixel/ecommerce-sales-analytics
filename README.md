# 🛒 E-Commerce Sales Performance Analytics

**Author:** Nithin Krishna | M.S. Business Analytics, UMass Isenberg  
**Tools:** Python · SQL · Tableau Public · Pandas · Statsmodels · Seaborn  
**Dataset:** Brazilian E-Commerce Public Dataset (Olist) — 100,000+ real orders (2016–2018)  
**Live Dashboard:** [View on Tableau Public](#) *(add link after publishing)*

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
| Total Revenue Analyzed | R$ 13.5M+ |
| Orders Analyzed | 96,478 delivered orders |
| Avg Order Value | R$ 140.32 |
| On-Time Delivery Rate | 92.1% |
| Avg Review Score | 4.09 / 5.0 |

**Top Insights:**
- Health & Beauty and Computers & Accessories are the top revenue categories — combined 31% of total
- Fast delivery (≤7 days) generates review scores 0.8 points higher than slow delivery (>21 days)
- OLS regression shows product price explains 67% of revenue variance (R² = 0.67, p < 0.001)
- São Paulo drives 42% of total revenue — highest concentration risk
- Champions segment (top RFM customers) represent 8% of customers but 34% of revenue

---

## 🔍 Analysis Structure

### 1. Data Cleaning & Merging
- Merged 7 relational tables into one analytical dataset
- Engineered features: delivery delay days, on-time flag, revenue per order
- Removed outliers: delivery > 120 days, revenue ≤ 0
- Final clean dataset: 96,478 records

### 2. Exploratory Data Analysis (7 Visualizations)
- Monthly revenue trend with 3-month rolling average
- Top 10 product categories by total revenue
- Review score distribution by delivery speed (boxplot)
- Correlation heatmap of key business metrics
- Revenue and avg order value by state (geographic analysis)
- OLS actual vs predicted revenue
- RFM customer segment distribution

### 3. OLS Regression — Revenue Drivers
```
Model: log(Revenue) ~ log(Price) + Freight + Delivery Days + Review Score + On Time

R² = 0.67 | F-statistic: 1,847 (p < 0.001)

Coefficients:
  log(Price):      +0.891  (p < 0.001) ✅ Strongest driver
  On Time:         +0.043  (p < 0.001) ✅ On-time delivery boosts revenue
  Freight Value:   +0.021  (p < 0.001) ✅ Freight included in order value
  Review Score:    +0.018  (p = 0.003) ✅ Higher scores → higher revenue
  Delivery Days:   -0.008  (p < 0.001) ✅ Longer delivery reduces revenue
```

### 4. RFM Customer Segmentation
| Segment | Customers | Avg Revenue |
|---|---|---|
| Champions | 4,823 (5%) | R$ 487 |
| Loyal Customers | 11,577 (12%) | R$ 312 |
| Potential Loyalists | 23,154 (24%) | R$ 198 |
| At Risk | 34,732 (36%) | R$ 134 |
| Lost Customers | 22,192 (23%) | R$ 89 |

---

## 📁 Repository Structure

```
ecommerce-sales-analytics/
├── Nithin_Ecommerce_Analysis.ipynb   ← Main analysis notebook
├── README.md                          ← This file
├── data/
│   └── data_source.md                 ← Dataset download instructions
├── visuals/
│   ├── visual1_revenue_trend.png
│   ├── visual2_category_revenue.png
│   ├── visual3_delivery_review.png
│   ├── visual4_correlation.png
│   ├── visual5_state_revenue.png
│   ├── visual6_regression.png
│   └── visual7_rfm.png
└── sql/
    └── business_queries.sql           ← 10 SQL business queries
```

---

## 🚀 How to Run

1. Open `Nithin_Ecommerce_Analysis.ipynb` in Google Colab
2. Click **Runtime → Run All**
3. Dataset downloads automatically — no setup needed
4. All 7 visualizations and regression output generate automatically

---

## 🛠️ Tech Stack

- **Python:** Pandas, NumPy, Seaborn, Matplotlib, Plotly, Statsmodels
- **SQL:** PostgreSQL-style queries for business KPIs
- **Tableau Public:** Interactive 5-page dashboard (live link above)
- **Google Colab:** Zero-setup reproducible environment

---

## 📬 Contact

**Nithin Krishna**  
nithinkrishna.km@gmail.com  
linkedin.com/in/nithin-krishna145  
github.com/nithink-pixel
