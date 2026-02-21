# 📊 Modern Data Warehouse Project (SQL Server)
📌 Project Overview

This project demonstrates how to design and implement a modern data warehouse using SQL Server to consolidate sales data from multiple source systems and enable analytical reporting.

The goal is to transform raw ERP and CRM data into a clean, structured, analytics-ready data model that supports business intelligence and decision-making.

Inspired by learning from Baraa Khatib Salkini ("Data With Baraa") on YouTube.

🎯 Objectives

Import data from multiple source systems (ERP & CRM)

Perform data cleansing and quality checks

Integrate data into a unified dimensional model

Enable SQL-based analytics for:

Customer Behavior

Product Performance

Sales Trends

Provide clear documentation for business and analytics teams

🏗️ Architecture Overview
🔹 Data Sources

ERP System (CSV files)

CRM System (CSV files)

🔹 Layers

Staging Layer

Raw data loaded directly from CSV files

No transformations applied

Data Warehouse Layer

Cleaned and transformed data

Star Schema design

Fact and Dimension tables

Analytics Layer

SQL queries for reporting and KPIs

Aggregations and business metrics

🗂️ Data Model (Star Schema)
📌 Fact Table

FactSales

SaleID

CustomerKey

ProductKey

DateKey

Quantity

SalesAmount

Cost

Profit

📌 Dimension Tables

DimCustomer

DimProduct

DimDate

DimSalesTerritory (if applicable)

This structure ensures optimized performance for analytical queries.

🔄 ETL Process
1️⃣ Extract

Import CSV files into staging tables using:

BULK INSERT

SSIS (optional)

OPENROWSET

2️⃣ Transform

Remove duplicates

Handle null values

Standardize formats (dates, text casing)

Validate relationships

Create surrogate keys

3️⃣ Load

Insert cleaned data into dimension tables

Populate fact table with foreign key references

📊 Business Intelligence & Reporting

Example insights generated from SQL:

📈 Sales Trends

Monthly revenue growth

Year-over-year comparison

Top-performing months

👥 Customer Analysis

Top customers by revenue

Customer segmentation

Repeat purchase behavior

🛍️ Product Performance

Best-selling products

Profit margin analysis

Category-level sales

🛠️ Technologies Used

Microsoft SQL Server

T-SQL

SQL Server Management Studio (SSMS)

CSV Data Sources

(Optional) Power BI for visualization

🚀 How to Run This Project

Clone the repository

Create a new database in SQL Server

Run the 01_Create_Tables.sql script

Load CSV files into staging tables

Run transformation scripts

Execute analytics queries

📁 Repository Structure
/data
   ├── erp_sales.csv
   ├── crm_customers.csv

/sql
   ├── 01_create_database.sql
   ├── 02_create_staging_tables.sql
   ├── 03_create_dw_tables.sql
   ├── 04_etl_transform_load.sql
   ├── 05_analytics_queries.sql

/docs
   └── data_model.png
📖 Learning Outcomes

Through this project, you will understand:

Data warehouse fundamentals

Star schema modeling

ETL design principles

Data quality management

SQL-based analytics

How to build a portfolio-ready data project

📜 License

This project is licensed under the MIT License.

You are free to use, modify, and distribute this project with proper attribution.

👨‍💻 About Me

Hi, I'm Preston 👋
Aspiring Data Engineer / Data Analyst passionate about building scalable data solutions and analytics platforms.

This project is part of my learning journey in data engineering and analytics.
