# Data-engineering-project
End-to-End Data Engineering Pipeline for Customer Demographics and Sales Analytics using Azure Cloud
# Project Overview
This project implements a comprehensive data engineering pipeline on Azure designed to address the business needs of understanding customer demographics, specifically focusing on gender distribution and its influence on product purchases. The pipeline extracts data from an on-premises SQL database, processes it using Azure Databricks, and loads it into Azure Synapse Analytics for reporting and analysis. The final data is visualized in an interactive Power BI dashboard, providing stakeholders with valuable insights into sales by gender and product category.
# Solution Overview
The solution is broken down into multiple components to address the requirements:

### Data Ingestion:

Extract data from an on-premises SQL database.
Load the data into Azure Data Lake Storage (ADLS) using Azure Data Factory (ADF).

### Data Transformation:

Use Azure Databricks to clean and transform the data.
Organize the data into Bronze, Silver, and Gold layers to ensure data quality and accessibility.

### Data Loading and Reporting:

Load the transformed data into Azure Synapse Analytics for efficient analysis.
Use Power BI to visualize KPIs related to sales by gender and product category, meeting business requirements.

### Automation:

Schedule the pipeline to run daily via ADF, ensuring stakeholders always have up-to-date data for reporting.
