"# Olist E-Commerce Databricks Lakehouse Analytics on Olist E-Commerce Dataset" 

📖 Project Overview
This project demonstrates an end-to-end data engineering and analytics workflow on the Olist e-commerce dataset using Databricks. 
It showcases core Databricks concepts including medallion architecture, Delta Lake optimizations, semantic views, and analytics dashboards.

Architecture
The project follows the Databricks Medallion Architecture:
Source Files → Bronze (raw ingestion) → Silver (cleaned & Transformed) → Gold (aggregated tables & views) → Databricks SQL Dashboard

Data Layers
**Bronze Layer**
- Raw ingestion of Olist dataset
- Schema preserved as-is

**Silver Layer**
- Data cleaning and enrichment
- Deduplication and joins
- Business-ready entities (orders, customers, products)

**Gold Layer**
- Aggregated fact and dimension tables
- Business metrics and KPIs
- Optimized using Delta Lake features
- Semantic and analytical views for dashboards

Gold Tables
- Customer metrics
- Product performance
- Orders fact
- Monthly sales trends

Gold Views for Dashboard
- KPI summary
- Revenue by state
- Monthly sales trends
- Payment distribution
- Delivery performance
- Top customers & products

Analytics & KPIs
**Core KPIs**
- Total Revenue
- Total Orders
- Average Order Value (AOV)

**Business Insights**
- Revenue distribution by state
- Monthly sales trends
- Customer payment behavior
- Delivery performance and fulfillment speed
- Top-performing products and customers

Databricks SQL Dashboard
An interactive dashboard built from Gold views:
- KPI tiles for executive summary
- Visualizations for revenue, trends, payments, and delivery
- Dashboard-level filters for interactive analysis
- Screenshots included in the repository

⚡Performance Optimization
- Delta Lake OPTIMIZE to reduce small files
- ZORDER on commonly filtered and joined columns
- Query performance validated using explain plans

🧪 Data Quality & Validation
- KPI values validated against Gold fact tables
- Basic data quality checks performed
- Clear separation between production analytics and learning queries
