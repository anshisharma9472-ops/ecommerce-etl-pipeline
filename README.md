# E-Commerce Sales ETL Pipeline & Analytics Dashboard

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.0-green)
![SQL](https://img.shields.io/badge/SQL-SQLite-orange)
![PowerBI](https://img.shields.io/badge/PowerBI-Dashboard-yellow)

## Project Overview

End-to-end ETL pipeline built on 100,000+ Brazilian 
e-commerce orders from Olist. Raw CSV files are extracted, 
cleaned, transformed, loaded into a SQL database, and 
visualized in an interactive Power BI dashboard.

## Business Problem

An e-commerce company needs to understand:
- Where is revenue coming from?
- Which products perform best?
- Why are customers not returning?
- How is delivery performance trending?

## Key Findings

| Finding | Value |
|---------|-------|
| Total Revenue | R$ 15.4 Million |
| Total Orders | 96,470 delivered |
| Customer Churn Rate | 97% one-time buyers |
| Top Category | Health & Beauty |
| Top State | São Paulo (37% revenue) |
| Avg Delivery Time | 12.09 days |
| Best Delivery Month | October 2016 (98.87%) |

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python | ETL scripting |
| Pandas | Data cleaning + transformation |
| SQLite + SQLAlchemy | Database + loading |
| SQL | KPI queries + views |
| Power BI | Interactive dashboard |
| Google Colab | Development environment |
| GitHub | Version control |

## Project Architecture

Raw CSV Files (8 files, 126MB)
↓
[EXTRACT] Python + Pandas
↓
[TRANSFORM] Data Cleaning

Convert date columns (6 columns)
Filter delivered orders only
Fix column name typos
Handle missing values
Remove duplicates
Merge 8 tables into master table
↓
[LOAD] SQLite Database
6 tables loaded
5 KPI SQL views created
↓
[VISUALIZE] Power BI Dashboard
5 interactive report pages

## Dashboard Pages

| Page | KPI |
|------|-----|
| Revenue Overview | Monthly trend, total revenue |
| Product Performance | Top categories, rankings |
| Regional Performance | Revenue by state, delivery |
| Customer Retention | Churn analysis, loyalty |
| Delivery Performance | On-time %, avg days |

## Dataset

Source: [Brazilian E-Commerce by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

| File | Rows |
|------|------|
| olist_orders_dataset.csv | 99,441 |
| olist_customers_dataset.csv | 99,441 |
| olist_order_items_dataset.csv | 112,650 |
| olist_order_payments_dataset.csv | 103,886 |
| olist_order_reviews_dataset.csv | 99,224 |
| olist_products_dataset.csv | 32,951 |
| olist_sellers_dataset.csv | 3,095 |
| olist_geolocation_dataset.csv | 1,000,163 |

> Raw data files are not included in this repo.
> Download from Kaggle link above.

## Project Structure

ecommerce-etl-pipeline/
│
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_cleaning.ipynb
│   ├── 03_transform.ipynb
│   ├── 04_load_sql.ipynb
│   ├── 05_sql_queries.ipynb
│   └── 06_kpi_views.ipynb
│
├── sql/
│   ├── kpi_monthly_revenue.sql
│   ├── kpi_top_products.sql
│   ├── kpi_regional_performance.sql
│   ├── kpi_customer_retention.sql
│   └── kpi_delivery_performance.sql
│
├── dashboard/
│   ├── ecommerce_dashboard.pbix
│   └── screenshots/
│
├── .gitignore
├── requirements.txt
└── README.md

## How to Run

```bash
# 1. Clone the repo
git clone https://github.com/YOUR_USERNAME/ecommerce-etl-pipeline.git

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download dataset from Kaggle
# Place CSVs in data/raw/

# 4. Run notebooks in order
# 01_eda → 02_cleaning → 03_transform → 
# 04_load_sql → 05_sql_queries → 06_kpi_views

# 5. Open dashboard
# Open dashboard/ecommerce_dashboard.pbix in Power BI
```    

## Author

**Anshika Sharma**
[LinkedIn](linkedin.com/in/anshika-sharma9472) | 
[GitHub](https://github.com/anshisharma9472-ops)                                                            
