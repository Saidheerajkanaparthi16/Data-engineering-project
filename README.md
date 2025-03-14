# Data-engineering-project
End-to-End Data Engineering Pipeline for Customer Demographics and Sales Analytics using Azure Cloud
# Project Overview
This project implements a comprehensive data engineering pipeline on Azure designed to address the business needs of understanding customer demographics, specifically focusing on gender distribution and its influence on product purchases. The pipeline extracts data from an on-premises SQL database, processes it using Azure Databricks, and loads it into Azure Synapse Analytics for reporting and analysis. The final data is visualized in an interactive Power BI dashboard, providing stakeholders with valuable insights into sales by gender and product category.
## Business Requirements
The business has identified a gap in understanding customer demographics—specifically, gender distribution and how it influences product purchases. The primary requirements include:

1. **Sales by Gende**r and **Product Category**: A dashboard showcasing total products sold, sales revenue, and gender split among customers.
2. **Data Filtering**: Allow stakeholders to filter by product category, gender, and date for comprehensive analysis.
3. **User-Friendly Interface**: Stakeholders should be able to easily interact with the data through Power BI, creating queries based on their preferences.
## Solution Overview
The solution is broken down into multiple components to address the requirements:

**Data Ingestion**: 
1. Extract data from an on-premises SQL database. 
2. Load the data into Azure Data Lake Storage (ADLS) using Azure Data Factory (ADF).

**Data Transformation**:
1. Use Azure Databricks to clean and transform the data.
2. Organize the data into Bronze, Silver, and Gold layers to ensure data quality and accessibility.

**Data Loading and Reporting**:
1. Load the transformed data into Azure Synapse Analytics for efficient analysis.
2. Use Power BI to visualize KPIs related to sales by gender and product category, meeting business requirements.

**Automation**: Schedule the pipeline to run daily via ADF, ensuring stakeholders always have up-to-date data for reporting.
