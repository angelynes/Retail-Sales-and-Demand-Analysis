# Retail Analytics & Operations Optimization 

## Overview 
This project contains an end-to-end retail analytics project designed to translate raw transactional records into actionable operational intelligence. Using R, this project implements predictive demand forecasting, market association mining, and customer behavioral segmentation to support data-driven decision-making in inventory management, store layout optimization, and targeted marketing campaigns. 

***Note:** To protect proprietary business information, all data in this repository has been rigorously anonymized. Customer names have been hashed, product identities have been globally shuffled, and financial/volume metrics have been scaled using random multipliers, while preserving the underlying statistical properties, mathematical frameworks, and code architecture.* 

## Technical Toolkit
*   **Language:** R
*   **Data Wrangling:** `tidyverse` (`dplyr`, `readr`, `lubridate`)
*   **Time Series & Machine Learning:** `tsibble`, `fable` (ARIMA models)
*   **Market Basket Analysis:** `arules` (Apriori algorithm)
*   **Visualization:** `ggplot2`, `plotly`

## Key Analyses & Business Impact

### 1. Demand Forecasting (ARIMA modeling)
*   **Objective:** Predict the next 4 weeks of sales for the top 10 highest-volume items.
*   **Methodology:** Converted random transaction timestamps into continuous weekly time-series data, filled timeline gaps, and ran an automated ARIMA model to calculate median expected sales alongside 80% and 95% statistical safety stock limits.
*   **Impact:** Replaced "gut feeling" purchasing with mathematical limits, preventing over-ordering and reducing inventory waste for highly perishable goods.

### 2. Market Basket Analysis (Apriori Algorithm)
*   **Objective:** Identify which specific products are most frequently purchased together to optimize store layout and promotions.
*   **Methodology:** Processed over 14,000 transactions through the Apriori algorithm, isolating high-confidence pairs and filtering out random purchases.
*   **Impact:** Discovered core anchor items and distinct vegetable/protein clusters. This guided the creation of grab-and-go meal kits and cross-selling scripts for staff, increasing overall basket size.

### 3. Customer Segmentation (RFM Analysis)
*   **Objective:** Identify the most valuable regulars and flag high-value customers at risk of churning.
*   **Methodology:** Scored known customers on a 1 to 5 curve based on Recency, Frequency, and Monetary value, segmenting them into distinct business categories (e.g., "VIP Regulars", "At-Risk VIPs"). 
*   **Impact:** Proved mathematically that loyalty members generate a disproportionate amount of revenue per visit compared to anonymous walk-ins. Generated an automated, ranked list of "At-Risk" customers for targeted WhatsApp win-back campaigns.

## Repository Structure
*   `data/`: Contains the anonymized and scaled `.csv` transaction datasets.
*   `Sales_Demand_Analysis.Rmd`: The complete RMarkdown analysis pipeline script. 
*   `Sales_Demand_Analysis.html`: The rendered HTML report complete with interactive visualizations. 
