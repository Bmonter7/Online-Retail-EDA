# Exploratory Data Analysis of UK Online Retail Transactions

## Project Overview

This repository contains an end-to-end exploratory data analysis of transactional data from a UK-based online retail store covering the period from December 2010 to November 2011. The goal is to uncover sales trends, customer behavior, and product performance, and to provide actionable recommendations that can guide strategic business decisions.

## Approach

My analysis followed a structured, business-focused workflow to ensure clarity and reproducibility:

1. **Data Loading & Inspection**  
   - Loaded the dataset from the provided Excel file and performed an initial review of its structure, missing values, and data types.

2. **Data Cleaning**  
   - Removed canceled orders and transactions with non-positive quantities or prices to ensure data integrity.  
   - Dropped records missing `CustomerID` and converted `InvoiceDate` to datetime format for accurate time series analysis.

3. **Feature Engineering**  
   - Created a `Revenue` column (`Quantity × UnitPrice`) to quantify line-item sales.  
   - Generated `InvoiceMonth` for monthly aggregations and `OrderValue` for invoice-level summaries.

4. **Exploratory Data Analysis**  
   - **Time Series Analysis:** Plotted monthly revenue trends to identify seasonality, peaks, and troughs.  
   - **Product & Customer Segmentation:** Ranked top products by revenue and quantity, and identified the highest-spending customers.  
   - **Geographic Insights:** Analyzed revenue distribution across countries, with a focus on export markets beyond the UK.

5. **Advanced Analysis**  
   - **Outlier Detection:** Used boxplots and percentile analysis to spot extreme `OrderValue` outliers and determine thresholds for capping.  
   - **Correlation Mapping:** Computed a heatmap of key metrics (`Quantity`, `UnitPrice`, `Revenue`, `OrderValue`) to uncover underlying relationships.

6. **Insight Synthesis & Recommendations**  
   - Translated analytical findings into strategic recommendations such as targeted promotions, inventory optimization, VIP customer programs, and export market focus.

Throughout the process, I prioritized transparency—retaining detailed code and narrative markdown cells to explain each decision. This approach not only demonstrates technical proficiency with Python and Pandas but also showcases business acumen in translating data into actionable insights.

## Key Insights

- **Seasonal Trends:** Identified April and February as slow months, a strong rebound in May–June, and a major revenue surge in Q4 (Sept–Nov).  
- **Best-Selling Products:** Discovered that specific décor items like "PAPER CRAFT", "LITTLE BIRDIE" and "REGENCY CAKESTAND 3 TIER" drive substantial revenue.  
- **Customer Concentration:** Top 10 customers contribute ~18% of total revenue, highlighting both opportunity and risk in customer dependency.  
- **Export Opportunities:** Netherlands, EIRE, Germany, France, and Australia are the most promising non-UK markets.  
- **Data Quality Notes:** Extreme outliers in order values (above ~£8K) were flagged for further investigation.

## Recommendations

1. **Smooth Out Seasonality:** Implement targeted promotions in slow months (Feb/Apr) and summer launches in May/Jun.  
2. **Optimize Inventory:** Prioritize and bundle top-revenue SKUs to maximize sales.  
3. **Customer Loyalty:** Introduce a VIP program for high-spend customers and diversify acquisition channels.  
4. **Expand Export Focus:** Allocate marketing resources to top export markets and tailor offers by average order size.  
5. **Manage Outliers:** Cap extreme order values above the 99th percentile when presenting typical metrics, and audit large orders for data integrity.
