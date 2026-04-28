# 🛒 Marketing Funnel & Conversion Performance Analysis
## Data Science & Analytics — Task 1 (2026)
### By Future Interns | Thembelihle Dladla

---

## 📌 Project Overview

This project analyzes **1M+ e-commerce events** from November 2019 to understand how users move through the marketing funnel — from page views to cart adds to purchases. The goal is to help the business identify drop-off points, optimize conversion rates, and grow revenue through data-driven decisions.

> **Dataset:** E-Commerce User Behavior Dataset | November 2019  
> **Tool:** Microsoft Power BI Desktop  
> **Pages:** 3 Interactive Dashboard Pages

---

## 🎯 Business Questions Answered

- Where are users dropping off in the funnel?
- Which brands and categories drive the most revenue?
- What price ranges convert best?
- Which hours of the day have the highest conversion rates?
- Where should the business focus to grow faster?

---

## 📊 Key Metrics at a Glance

| Metric | Value |
|--------|-------|
| 👁 Total Page Views | 1,014,762 |
| 🛒 Total Cart Adds | 15,445 |
| 💳 Total Purchases | 18,368 |
| 💰 Total Revenue | $5,653,876 |
| 🧾 Avg Order Value | $307.81 |
| 👥 Unique Buyers | 13,635 |
| 📉 View → Cart Rate | 1.52% |
| 🎯 Overall Conv Rate | 1.81% |

---

## 📁 Dashboard Structure

### 📄 Page 1 — Executive Overview
The main performance dashboard providing a high-level summary of all funnel metrics.

**Visuals included:**
- KPI Cards — Total Views, Cart, Purchases, Revenue, AOV
- Total Views by Hour (Area Chart)
- Total Purchases by Time of Day — Morning, Afternoon, Evening, Night
- Total Revenue by Category (Bar Chart)
- Conversion rate of brand by Time of Day

---

### 📄 Page 2 — Conversion & Revenue Deep Dive
Detailed breakdown by brand, category, and price range to identify top performers and underperformers.

**Visuals included:**
- Price Range Table — Views, Purchases, Conv Rate %, Revenue, Funnel Status
- Category Table — Top 14 categories with Conv Rate and Category Status
- Top 10 Brands by Total Revenue (Clustered Bar Chart)
- Revenue by Categories (Bar Chart)
  
---

### 📄 Page 3 — Funnel Insights & Growth Recommendations
Data-driven actions to improve conversion and revenue,
with visual drop-off analysis at each funnel stage.

**Visuals included:**

- **Funnel Drop-off Analysis** (Bar Chart)
  - X-axis: Stage — View → Cart / Cart → Purchase
  - Y-axis: Drop-off rate (0.0 to 1.0 scale)
  - Shows View → Cart as the critical drop-off stage

- **Conversion Value by Stage** (Bar Chart)
  - X-axis: Stage — Cart → Purchase / View → Cart
  - Y-axis: Conversion Value
  - Cart → Purchase performs strongest at 1.19

- **Drop-off Stage Table**
  - Columns: Stage, Drop Value, Drop Label,
    Drop-off Status, Stage Recommendation
  - View → Cart: 0.98 drop | 98.5% | 🔴 Critical |
    Improve product engagement
  - Cart → Purchase: -0.19 drop | -18.9% | 🟢 Good |
    Performing well
  - Total row with overall status

- **KPI Card — Lost Users**
  - Value: 996K
  - Users who viewed but never converted

- **KPI Card — Drop Off Rate**
  - Value: 98.48%
  - Overall funnel drop-off rate

---

## 🔍 Key Findings

### 1. 🔴 Massive Top-Funnel Drop-Off
**98.5% of visitors never add to cart.** This is the single biggest issue — fixing product discovery and engagement at the top of the funnel has the highest potential revenue impact.

### 2. ⭐ Peak Conversion: 06:00–10:00 UTC
Conversion rate is **80% higher in morning hours** (2.1–2.3%) compared to afternoon (1.2%). Ad budgets should shift to this window immediately.

### 3. 📦 Electronics Dominates at 76.9%
Electronics drives **$4.35M of the $5.65M** total revenue. Smartphones alone account for $3.9M. Both a massive opportunity and a concentration risk.

### 4. 🍎 Apple vs Samsung
Apple converts at **3.70%** vs Samsung's **3.58%** despite Samsung having 27% more views. Apple customers show stronger purchase intent.

### 5. 💲 $101–$200 Price Range = Best Conversion
The **$101–$200 price band** has the highest conversion rate at **2.12%**. The $51–$100 range underperforms at 1.42% and needs attention.

### 6. 👗 Apparel is Broken
**40,545 views but only 0.31% conversion** — the lowest of any category. The UX, pricing, or product range for apparel needs urgent review.

---

## ⚡ Top 7 Recommendations

| Priority | Area | Action | Expected Impact |
|----------|------|--------|----------------|
| 🥇 1 | Top Funnel | Add exit-intent popups & product recommendations | 📈 2× Revenue |
| 🥈 2 | Ad Timing | Shift 40% of budget to 06:00–10:00 UTC | 📈 40% better ROAS |
| 🥉 3 | Electronics | Create Phone + Headphone bundles | 📈 +$93 per order |
| 4️⃣ | Price Range | A/B test $51–$100 price anchoring | 📈 +0.5% conv rate |
| 5️⃣ | Brand | Samsung cart retargeting campaign | 📈 +$200K revenue |
| 6️⃣ | Apparel | Full UX audit of apparel pages | 📈 Fix broken category |
| 7️⃣ | Checkout | Make Buy Now button more prominent | 📈 +15% purchases |

---

## 🛠 Tools & Technologies Used

| Tool | Purpose |
|------|---------|
| **Power BI Desktop** | Interactive dashboard & visualization |
| **Power Query (M Language)** | Data cleaning & transformation |
| **DAX** | Calculated columns, measures & KPIs |
| **Microsoft Excel** | Initial data exploration |
| **Python (Pandas)** | Advanced analysis & data validation |

---

## 📐 DAX Measures Created

| Category | Measures |
|----------|---------|
| Funnel KPIs | Total Views, Total Cart Adds, Total Purchases, Total Revenue, AOV |
| Conversion Rates | View→Cart Rate, Cart→Purchase Rate, Overall Conv Rate, Cart Abandonment |
| Brand Analysis | Brand Revenue, Brand Conv Rate, Brand Market Share, Top 10 Flag |
| Category Analysis | Category Revenue, Category Rank, Category Status, Top 10 Flag |
| Price Analysis | Price Range Conv Rate, Price Range Revenue Share, Price Range Status |
| Time Analysis | Conv Rate by Hour, Peak Hour Flag, Time of Day grouping |
| Status Labels | Funnel Status, Category Status, Revenue Status, Performance Status |

---

## 🔄 Power Query Transformations

| Transformation | Description |
|---------------|-------------|
| Remove UTC text | Cleaned `event_time` column from text to datetime |
| Fill nulls — category | Replaced blank `category_code` with `"unknown"` |
| Fill nulls — brand | Replaced blank `brand` with `"other"` |
| Add `category_main` | Extracted first level — Electronics, Appliances etc. |
| Add `category_label` | Full readable path — Electronics › Smartphone |
| Add `brand_clean` | Title-cased brand names |
| Add `hour` | Extracted hour from datetime |
| Add `time_of_day` | Morning / Afternoon / Evening / Night grouping |
| Add `price_bucket` | $0-$50, $51-$100, $101-$200, $201-$500, $501-$1K, $1K+ |

---

## 📈 Funnel Drop-Off Summary

```
👁 Page Views        1,014,762   (100%)
        ↓ 98.48% drop-off
🛒 Cart Adds            15,445   (1.52%)
        ↓ Strong close rate
💳 Purchases            18,368   (1.81% of views)
        ↓
👤 Unique Buyers         13,635
```

> ⚠️ Note: Purchases exceed cart adds because the dataset includes direct "Buy Now" purchases that bypass the cart — a positive signal showing strong impulse purchase behavior.

---

## 🚀 How to Use This Dashboard

1. Download `Task 3.pbix` from this repository
2. Open with **Power BI Desktop** (free download at powerbi.microsoft.com)
3. The data is embedded — no external connections needed
4. Navigate between **3 pages** using the tabs at the bottom
5. Use the **slicers** to filter by category, brand, price range, or time of day
6. Hover over any visual for **detailed tooltips**

### System Requirements
- Power BI Desktop (latest version recommended)
- Windows 10/11
- Minimum 4GB RAM

---

## 📂 Repository Structure

```
marketing-funnel-analysis/
│
├── 📊 Task_1.pbix                    # Power BI Dashboard (main file)
│
├── 📁 data/
│
├── 📁 screenshots/
│   ├── page1_overview.png  # Page 1 screenshot
│   ├── page2_conversion_analysis.png # Page 2 screenshot
│   └── page3_Data_driven_actions.png  # Page 3 screenshot
│
└── README.md                        # This file
```

---

## 📚 Dataset Information

| Field | Description |
|-------|-------------|
| `event_time` | Timestamp of the event |
| `event_type` | view / cart / purchase |
| `product_id` | Unique product identifier |
| `category_id` | Category identifier |
| `category_code` | Full category path (e.g. electronics.smartphone) |
| `brand` | Product brand name |
| `price` | Product price in USD |
| `user_id` | Unique user identifier |
| `user_session` | Session identifier |

**Source:** E-Commerce Behavior Data | Kaggle  
**Period:** November 2019  
**Size:** 1,048,575 rows × 9 columns

---

## 👤 Author

**Thembelihle Dladla**

- 💼 LinkedIn: https://www.linkedin.com/in/thembelihle-dladla-1272a7292/
- 🌐 GitHub: [@lihledladla98](https://github.com/lihledladla98)
- 📧 Email: lihledladla98.email@gmail.com

---

## 🏢 Program

Future Interns — Data Science & Analytics Program 2026

---

## 🏷 Tags

`power-bi` `data-analytics` `marketing-funnel` `conversion-analysis`
`ecommerce` `dax` `power-query` `business-intelligence`
`future-interns` `data-science` `python` `excel`

---

*This project was completed as part of the Future Interns Data Science & Analytics internship program. All analysis is based on publicly available e-commerce behavior data.*
