# Retail Analytics & Operations Optimization

## Overview

This project presents an end-to-end retail analytics workflow that transforms transactional sales data into actionable business insights.

Using R, the analysis combines demand forecasting, market basket analysis, and customer segmentation to support decisions in inventory planning, merchandising, customer retention, and marketing.

> **Data Privacy:** To protect proprietary business information, all data in this repository has been anonymized. Customer identities were hashed, product identities were shuffled, and sensitive financial and volume metrics were scaled while preserving the analytical structure required for the methods demonstrated in this project.

## Technical Toolkit

- **Language:** R
- **Data Wrangling:** `tidyverse`, `dplyr`, `readr`, `lubridate`
- **Time Series Forecasting:** `tsibble`, `fable` — ARIMA
- **Market Basket Analysis:** `arules` — Apriori algorithm
- **Visualization:** `ggplot2`, `plotly`
- **Reporting:** R Markdown

## Key Analyses

### 1. Demand Forecasting

**Business Question:**  
How much inventory should be purchased for high-volume products over the next four weeks?

**Approach:**  
- Aggregated transaction data into continuous weekly time series
- Filled missing periods to maintain consistent temporal structure
- Identified the 10 highest-volume products
- Fit automated ARIMA models using `fable`
- Generated four-week forecasts with 80% and 95% prediction intervals

**Business Application:**  
Forecast ranges were used to inform purchasing and safety-stock decisions, replacing intuition-based ordering with a more structured inventory-planning process.

---

### 2. Market Basket Analysis

**Business Question:**  
Which products are frequently purchased together, and how can those relationships support merchandising and cross-selling?

**Approach:**  
- Processed more than 14,000 transactions
- Applied the Apriori algorithm to identify recurring product combinations
- Evaluated association rules using support, confidence, and lift
- Filtered low-value associations to focus on commercially meaningful purchasing patterns

**Business Application:**  
The analysis identified anchor products and recurring product clusters that informed product placement, bundle ideas, and cross-selling opportunities.

---

### 3. Customer Segmentation

**Business Question:**  
Who are the most valuable customers, and which high-value customers may be at risk of becoming inactive?

**Approach:**  
- Calculated Recency, Frequency, and Monetary metrics for identified customers
- Assigned RFM scores from 1–5
- Grouped customers into actionable segments such as:
  - VIP Regulars
  - Loyal Customers
  - At-Risk VIPs
  - Inactive Customers
- Generated ranked customer lists for retention outreach

**Business Application:**  
The analysis quantified differences in purchasing behavior between customer segments and created a structured way to prioritize retention and win-back campaigns.

## Repository Structure

```text
Retail-Sales-and-Demand-Analysis/
│
├── data/
│   └── anonymized transaction datasets
│
├── Sales_Demand_Analysis.Rmd
│   └── complete analysis and modeling pipeline
│
├── Sales_Demand_Analysis.html
│   └── rendered report with interactive visualizations
│
└── README.md
