# 🛒 E-Commerce Sales Analysis: Python + Power BI

An end-to-end data analytics project: a raw Kaggle sales dataset is cleaned and explored in **Python**, exported to **Excel**, and visualised in an interactive three-page **Power BI** dashboard.

<!-- Add a dashboard screenshot here: ![Dashboard Preview](dashboard/preview.png) -->

---

## 📌 Project Overview

| | |
|---|---|
| **Goal** | Understand sales, profit and customer payment behaviour across products and regions |
| **Period** | January – December 2023 |
| **Records** | 305 raw rows → 300 clean orders |
| **Tools** | Python (pandas, NumPy, Matplotlib), Google Colab, Excel, Power BI Desktop |

## 🔑 Key Metrics

| Metric | Value |
|---|---|
| Total sales | ₹1.19M |
| Total profit | ₹351K |
| Profit margin | 29.54% |
| Total units sold | 1,668 |
| Top product (by quantity) | Keyboard (254 units) |

## 💡 Key Insights

- **Regional sales are evenly spread.** West leads (₹293K), then East (₹283K), South (₹280K) and North (₹278K), with only a small gap between them.
- **Electronics earns more profit than Accessories** (₹182.5K vs ₹168.9K).
- **October is the peak month** (₹143.9K), and July is the weakest (₹68.6K).
- **Card is the most-used payment method**: ₹470K across 108 orders, ahead of Cash (₹390K, 95 orders) and Transfer (₹330K, 97 orders).
- **Keyboard sells the most units**, followed by Tablet (222) and Mouse (208).
- **About 5% of sales (₹56K) have no region recorded.** This is a data-quality gap worth fixing at the source.

---

## 🧹 Data Cleaning (Python)

1. Standardised column names (strip whitespace, lowercase)
2. Removed **5 duplicate rows** (305 → 300)
3. Filled **10 missing `region`** values with `Unknown`
4. Filled **10 missing `payment_method`** values with the most frequent value (mode)
5. Converted `order_date` to datetime
6. Engineered features: `day`, `month`, `year`, `profit_margin` (%)
7. Exported the final dataset to `cleaned_data.xlsx`

## 📊 Exploratory Analysis

- Sales by region (bar and pie charts)
- Profit by category
- Monthly sales trend (line chart)
- Sales and profit distributions (histograms)
- Top-selling products by quantity (bar chart)

## 📈 Power BI Dashboard

The dashboard has three linked pages with navigation buttons and **day / month / year** slicers.

| Page | Visuals |
|---|---|
| **Dashboard** | KPI cards, monthly trend, sales by region (pie), product slicer, product sales table with images, sales by payment method |
| **Sales** | Decomposition tree (Region → Product), bubble chart of profit vs. profit margin by product |
| **Payment** | Payment method vs. sales, treemap of products by payment method, payment count table |

**Techniques used:** DAX measures (profit margin, top product), page navigation, slicers, decomposition tree, treemap, bubble chart, combo chart.

---

## 📁 Repository Structure

```
ecommerce-sales-dashboard/
├── data/
│   ├── raw/                    # Original Kaggle dataset
│   └── processed/
│       └── cleaned_data.xlsx   # Cleaned output from the notebook
├── notebooks/
│   └── Sales_analysis.ipynb    # Cleaning + EDA
├── dashboard/
│   ├── E-Commerce_Dashboard.pdf
│   └── E-Commerce_Dashboard.pbix   # add your Power BI file here
└── README.md
```

*If you found this project useful, consider giving it a ⭐*
