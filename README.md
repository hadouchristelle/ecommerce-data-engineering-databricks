# # E-Commerce Batch & Streaming Data Engineering Pipeline with Databricks
End-to-End E-Commerce Data Engineering Project using Batch Processing, Auto Loader Streaming, PySpark, Delta Lake, Unity Catalog, Spark SQL, and Databricks Workflows
This project demonstrates the development of an end-to-end E-Commerce Data Engineering pipeline using Databricks.

## 📌 Project Overview

The solution processes e-commerce data through both batch and incremental streaming ingestion. Databricks Auto Loader is used to automatically detect and process newly arriving files, while checkpoints and schema tracking are used to maintain reliable incremental ingestion.
The project follows the Medallion Architecture, organizing data into Bronze, Silver, and Gold layers. PySpark is used for data cleaning, transformation, filtering, aggregation, duplicate handling, missing-value management, and data quality processing.
Delta Lake is used to provide reliable data storage and advanced capabilities such as ACID transactions, schema enforcement, table history, Time Travel, and data optimization.
Unity Catalog is used to organize and govern data assets through catalogs, schemas, tables, and volumes. Spark SQL is used for analytical queries, while Databricks Workflows orchestrates the different stages of the pipeline.

## 🎯 Business Objective

The main objective of this project is to transform raw e-commerce data
into reliable and structured datasets that can support sales analysis,
customer behavior analysis, and product performance monitoring.
## ❓ Business Questions

- Which product categories generate the highest sales?
- Which products and categories generate the highest profit?
- How does customer purchasing behavior vary across markets?
- What is the average sales value per order?
- What trends and anomalies can be identified in sales and profit data?
  ## 🏗️ Architecture
  <img width="1482" height="731" alt="Diagramme sans nom" src="https://github.com/user-attachments/assets/93a827e8-581a-40f9-8b03-1eedc89641a4" />
  ## Technologies

- Databricks
- Apache Spark
- PySpark
- Spark SQL
- Delta Lake
- Unity Catalog
- Python
  
  ## Data Processing

  The project includes:

- CSV, JSON, and Parquet ingestion
- PySpark DataFrame transformations
- Data type conversion
- Null handling
- Duplicate removal
- Filtering and aggregations
- String and date functions
- Delta Lake operations
- Time Travel
- Z-Ordering
- Spark SQL analytics
## 🔄 Databricks Workflow Orchestration

To automate and orchestrate the E-Commerce data pipeline, I created a Databricks Workflow named **`Ecommerce_Data_Pipeline`**.

The workflow coordinates three main processing stages:

1. **01_Data_Ingestion** – Ingests the source e-commerce data.
2. **02_Data_Transformation** – Cleans and transforms the data using PySpark.
3. **03_Data_Analytics** – Processes the transformed data for analytical use.

The workflow manages the execution of these tasks as part of a single data pipeline, making the process easier to monitor, troubleshoot, and maintain.

During testing, some workflow runs failed due to execution issues. After troubleshooting and correcting the pipeline, the workflow completed successfully.

### Workflow Execution

![Databricks Workflow](screenshots/workflow/ecommerce_workflow.png)

The successful execution confirms that the different stages of the pipeline can be orchestrated and monitored through Databricks Workflows.
  
