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
![arch-Photoroom](https://github.com/user-attachments/assets/07c87862-8d95-44fd-b0c6-e60d6e8aa4d3)

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

## Technology Stack

+ **Azure Data Factory (ADF)**: For orchestrating data movement and transformation.
+ **Azure Data Lake Storage (ADLS)**: For storing raw and processed data.
+ **Azure Databricks**: For data processing and transformation.
+ **Azure Synapse Analytics**: For data warehousing and SQL-based analytics.
+ **Power BI**: For interactive data visualization.
+ **Azure Key Vault**: For managing credentials and secrets securely.
+ **SQL Server (On-Premises)**: Source of customer and sales data.
  
## Setup Instructions
**Prerequisites**
+ An Azure account with sufficient credits.
+ Access to an on-premises SQL Server database, preferably with AdventureWorks database restored.
### Step 1: Azure Environment Setup
1. Create a new Resource Group in Azure.
2. Provision the following services:
   _ Azure Data Factory (ADF).
   _ Azure Data Lake Storage (ADLS) with bronze, silver, and gold containers.
   _ Azure Databricks and Azure Synapse Analytics workspaces.
   _ Azure Key Vault for managing secrets.

### Step 2: Data Ingestion

1. **SET UP SQL SERVER** :Install SQL Server and SQL Server Management Studio (SSMS). Restore the AdventureWorks database.
2. **Ingest data with ADF** :Use ADF to create pipelines for extracting data from SQL Server to ADLS (bronze layer).

### Step 3: Data Transformation

1.**Mount data in Databricks**: Mount ADLS in Azure Databricks.

2.**Transform Data**: Cleanse and transform data using Databricks Notebooks:
Process data from bronze to silver (cleansed) and gold (aggregated).

### Step 4: Data Loading and Reporting

1. **Load Data into Synapse** : Set up a Synapse SQL pool and load gold layer data for reporting.
2. **Create Power BI Dashboard**: Build Power BI reports to visualize sales performance by gender and product category.

### Step 5: Automation and Monitoring

1. **Schedule Pipelines**: Use ADF to schedule the data pipeline to run daily.
2. **Monitor Pipelines**: Monitor pipeline execution using ADF and Synapse monitoring tools.
   
### Step 6: Security and Governance

1. **Manage Access**: Configure Role-Based Access Control (RBAC) using Azure Active Directory (Entra ID

### Step 7: End-to-End Testing

1. **Trigger and Test Pipelines**: Insert new records into SQL Server and verify if the data pipeline runs successfully.
Ensure Power BI is updated with the latest data and insights.

## Conclusion

This project implements a data pipeline that allows businesses to track sales trends based on gender and product category, providing actionable insights. The pipeline automates the process, ensuring stakeholders always have up-to-date data. By utilizing Azure services, this solution enhances da
