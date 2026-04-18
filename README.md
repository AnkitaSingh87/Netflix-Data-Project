
**Netflix Data Project**
------------------------------

**📌 Overview**

This project demonstrates an end-to-end ETL pipeline for Netflix data using Azure Data Factory (ADF) for ingestion, Databricks Delta Live Tables (DLT) for transformation, and Power BI for visualization. The goal is to showcase a modern cloud-based data engineering workflow that ingests raw data, processes it into curated layers, and enables business insights.

**🚀 Architecture**

1. Data Ingestion (Azure Data Factory)
   

<img width="800" height="400" alt="Screenshot 2026-04-11 153543" src="https://github.com/user-attachments/assets/937f7586-e698-4916-9854-fdee34822973" />





--Raw Netflix dataset ingested from source into Azure Data Lake.

--Pipelines orchestrated in ADF with linked services and datasets.

--Publish configuration managed via publish_config.json.

2. Data Transformation (Databricks + Delta Live Tables)


 <img width="800" height="400" alt="Screenshot 2026-04-12 170843" src="https://github.com/user-attachments/assets/089e140b-6be5-45f1-a6e7-d39a03330894" />


--Raw data validated and cleaned using PySpark scripts (spark_scripts.dbc).

--Implemented Medallion Architecture:

   Bronze Layer: Raw ingestion.

   Silver Layer: Cleaned and deduplicated data.

   Gold Layer: Aggregated and business-ready tables.
   

  <img width="800" height="400" alt="Screenshot 2026-04-18 190230" src="https://github.com/user-attachments/assets/4c5daa81-cad5-43d7-a7a9-93e13b2189ee" />



   Applied transformations such as:

   Schema enforcement

   Deduplication

   Data quality checks

   Ranking and categorization
   

3. Data Storage (Delta Lake)

--Data stored in Delta Lake tables for ACID transactions and scalable queries.

--Checkpointing and streaming enabled for reliability.

4. Visualization (Power BI)

--Curated Gold layer exposed to Power BI.

--Dashboards built to analyze Netflix content trends, genres, and performance metrics.


**⚙️ Technologies Used**

Azure Data Factory (ADF) – Orchestration and ingestion.

Databricks (DLT) – Transformation and pipeline automation.

Delta Lake – Reliable storage with ACID transactions.

Power BI – Visualization and reporting.

PySpark – Data processing and ETL logic.


**📊 Key Features**

End-to-end cloud ETL pipeline.

Delta Live Tables for automated data quality and lineage.

Medallion architecture implementation.

Integration with Power BI for insights.

Modular and reusable pipeline design.


**📈 Business Impact**

Enables data-driven insights into Netflix content trends.

Demonstrates scalable and reliable ETL pipelines.

Showcases integration of Azure + Databricks + Power BI for modern analytics.
