🧾 Vendor Performance Analysis – Retail Inventory & Sales

Analyzing vendor efficiency and profitability to support strategic purchasing and inventory decisions using SQL, Python, and Power BI.

📌 Table of Contents

Overview

Business Problem

Dataset

Tools & Technologies

Project Structure

Data Cleaning & Preparation

Exploratory Data Analysis (EDA)

Research Questions & Key Findings

Dashboard

How to Run This Project

Final Recommendations

Author & Contact

Overview

This project evaluates vendor performance and retail inventory dynamics to generate actionable insights for purchasing, pricing, and inventory optimization.

An end-to-end data pipeline was built using:

SQL for ETL and transformations

Python for analysis and hypothesis testing

Power BI for visualization

Business Problem

Effective inventory and sales management are critical in retail. This project aims to:

Identify underperforming brands requiring pricing or promotional adjustments

Determine vendor contributions to sales and profit

Analyze the cost-benefit of bulk purchasing

Investigate inventory turnover inefficiencies

Statistically validate differences in vendor profitability

Dataset

Multiple CSV files located in /data/ (sales, vendors, inventory)

Summary tables created from ingested data and used for downstream analysis

Tools & Technologies

SQL – CTEs, Joins, Filtering

Python – Pandas, Matplotlib, Seaborn, SciPy

Power BI – Interactive dashboards

GitHub – Version control

Project Structure
vendor-performance-analysis/
│
├── README.md
├── .gitignore
├── requirements.txt
├── Vendor Performance Report.pdf
│
├── notebooks/
│   ├── exploratory_data_analysis.ipynb
│   └── vendor_performance_analysis.ipynb
│
├── scripts/
│   ├── ingestion_db.py
│   └── get_vendor_summary.py
│
├── dashboard/
│   └── vendor_performance_dashboard.pbix

Data Cleaning & Preparation

Removed transactions with:

Gross Profit ≤ 0

Profit Margin ≤ 0

Sales Quantity = 0

Created vendor-level summary metrics

Converted data types

Handled outliers

Merged lookup tables

Exploratory Data Analysis (EDA)
Negative / Zero Values

Gross Profit: Min -52,002.78 (loss-making sales)

Profit Margin: Min -∞ (zero or below-cost sales)

Unsold Inventory indicated slow-moving stock

Outliers

Freight costs up to 257K

Extreme purchase and actual prices

Correlations

Strong between Purchase Qty & Sales Qty (0.999)

Weak between Purchase Price & Profit

Negative between Profit Margin & Sales Price (-0.179)

Research Questions & Key Findings

Brands for Promotions
→ 198 brands showed low sales but high margins

Top Vendors
→ Top 10 vendors account for 65.69% of purchases (concentration risk)

Bulk Purchasing Impact
→ ~72% unit cost savings on large orders

Inventory Turnover
→ $2.71M worth of unsold inventory identified

Vendor Profitability

Category	Mean Margin
High Vendors	31.17%
Low Vendors	41.55%

Hypothesis Testing
Statistically significant difference in profit margins → distinct vendor strategies confirmed

Dashboard

Power BI dashboard visualizes:

Vendor-wise sales and margins

Inventory turnover

Bulk purchase savings

Performance heatmaps

How to Run This Project

Clone repository:

git clone https://github.com/yourusername/vendor-performance-analysis.git


Install dependencies:

pip install -r requirements.txt


Load CSVs and ingest:

python scripts/ingestion_db.py


Create vendor summary:

python scripts/get_vendor_summary.py


Run notebooks:

notebooks/exploratory_data_analysis.ipynb

notebooks/vendor_performance_analysis.ipynb

Open Power BI dashboard:

dashboard/vendor_performance_dashboard.pbix

Final Recommendations

Diversify vendor base to reduce dependency risk

Optimize bulk order strategies

Reprice slow-moving, high-margin brands

Clear unsold inventory strategically

Improve marketing for underperforming vendors

Author & Contact

Raj Nandini
Data Analyst

📧 Email: rajnandini7802@gmail.com

🔗 LinkedIn: https://www.linkedin.com/in/rajnandini02
