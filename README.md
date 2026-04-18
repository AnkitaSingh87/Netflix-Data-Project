
Netflix Data Project

📌 Overview

This project demonstrates an end-to-end ETL pipeline for Netflix data using Azure Data Factory (ADF) for ingestion, Databricks Delta Live Tables (DLT) for transformation, and Power BI for visualization. The goal is to showcase a modern cloud-based data engineering workflow that ingests raw data, processes it into curated layers, and enables business insights.

🚀 Architecture

1. Data Ingestion (Azure Data Factory)

Raw Netflix dataset ingested from source into Azure Data Lake.

Pipelines orchestrated in ADF with linked services and datasets.

Publish configuration managed via publish_config.json.

2. Data Transformation (Databricks + Delta Live Tables)

Raw data validated and cleaned using PySpark scripts (spark_scripts.dbc).

Implemented Medallion Architecture:

Bronze Layer: Raw ingestion.

Silver Layer: Cleaned and deduplicated data.

Gold Layer: Aggregated and business-ready tables.

Applied transformations such as:

Schema enforcement

Deduplication

Data quality checks

Ranking and categorization

3. Data Storage (Delta Lake)

Data stored in Delta Lake tables for ACID transactions and scalable queries.

Checkpointing and streaming enabled for reliability.

4. Visualization (Power BI)

Curated Gold layer exposed to Power BI.

Dashboards built to analyze Netflix content trends, genres, and performance metrics.

📂 Repository Structure

Raw Data/ → Contains raw Netflix dataset.

factory/ → Azure Data Factory pipeline definitions.

linkedService/ → Linked service configurations.

pipeline/ → Pipeline JSON definitions.

spark_scripts.dbc → Databricks notebooks for transformations.

publish_config.json → Deployment configuration for ADF.

⚙️ Technologies Used

Azure Data Factory (ADF) – Orchestration and ingestion.

Databricks (DLT) – Transformation and pipeline automation.

Delta Lake – Reliable storage with ACID transactions.

Power BI – Visualization and reporting.

PySpark – Data processing and ETL logic.

📊 Key Features

End-to-end cloud ETL pipeline.

Delta Live Tables for automated data quality and lineage.

Medallion architecture implementation.

Integration with Power BI for insights.

Modular and reusable pipeline design.

🛠️ How to Run

Clone the repository:

git clone https://github.com/AnkitaSingh87/Netflix-Data-Project.git

Deploy ADF pipelines using factory/ and pipeline/ JSON files.

Import spark_scripts.dbc into Databricks workspace.

Configure Delta Live Tables for Bronze, Silver, and Gold layers.

Connect Power BI to Gold layer tables for visualization.

📈 Business Impact

Enables data-driven insights into Netflix content trends.

Demonstrates scalable and reliable ETL pipelines.

Showcases integration of Azure + Databricks + Power BI for modern analytics.
