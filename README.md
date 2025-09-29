# Azure-Data-Pipeline-Hub

📌 # Project Overview

This project demonstrates an end-to-end Azure Data Engineering pipeline using the AdventureWorks dataset. It follows the medallion architecture (Bronze → Silver → Gold) to ingest, transform, and model data for analytics and reporting.

The main goal is to build a scalable cloud data pipeline capable of handling raw data ingestion, transformation, and consumption-ready data for BI tools.



🏗️ # Architecture

Data Ingestion (Bronze Layer)

Source: AdventureWorks CSV files (Products, Customers, Sales, Returns, Territories, Calendar).

Stored in Azure Data Lake Storage (ADLS Gen2).

Configuration handled using git.json, mapping dataset names to sink folders and files.

Data Transformation (Silver Layer)

Applied using PySpark/Notebooks (silver_layer_refer.ipynb).

Cleansed, validated, and standardized data.

Joins and transformations to prepare data for analytics.

Data Modeling (Gold Layer)

Created SQL Views using Synapse Serverless SQL Pools.

Script: Create Views Gold.sql

Gold layer provides business-ready tables such as:

gold.calendar

gold.customers

gold.products

gold.sales

gold.returns

gold.subcat

gold.territories



⚙️ # Tech Stack

Azure Data Lake Storage (ADLS Gen2) – Raw/Silver/Gold data layers

Azure Synapse Analytics – SQL views for gold layer

Azure Data Factory – Orchestration & pipeline automation

Databricks / PySpark Notebooks – Silver layer transformation

Power BI / Reporting Tools – Data consumption layer

SQL, Python, JSON

📊 Data Flow (Medallion Architecture)

Bronze (Raw) → Silver (Cleansed) → Gold (Business-ready)

Bronze Layer: CSV ingestion from GitHub into ADLS.

Silver Layer: Transformation with PySpark Notebook (silver_layer_refer.ipynb).

Gold Layer: SQL Views created in Synapse (Create Views Gold.sql).



🚀 Key Features

✅ Automated data ingestion from GitHub/CSV sources.

✅ Data cleaning & transformation with PySpark.

✅ Business-ready data models with Synapse SQL Views.

✅ Scalable cloud-first solution using Azure Data Engineering stack.

✅ Supports analytics & reporting (e.g., Power BI dashboards).



📈 # Example Use Cases

Sales performance tracking by region & time.

Customer segmentation analysis.

Product performance & return trends.

Territory-based reporting for business insights.



🔮 # Future Enhancements

Add CI/CD pipeline using Azure DevOps/GitHub Actions.

Implement Delta Lake for improved ACID transactions.

Deploy ML models (Predictive Analytics) on top of Gold layer data.


👨‍💻 # Author

# Mohammad Shoaib
💡 Exploring Data Engineering | Data Science | Machine Learning | Generative AI
