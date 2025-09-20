# Data Engineering using Microsoft Fabric and Reporting using PowerBI on Worldwide Earthquake data from USGS: End-to-End Data Engineering Project with Business Reporting
## Introduction
Having been DP-700 Certified (Microsoft Fabric Data Engineer Associate), I wanted to work on an end-to-end Data Engineering project along with business reporting in Microsoft Fabric.
This project aims to process(ETL) earthquake data and create an interactive PowrBI visualization. 
Dataset Source: USGS site - https://earthquake.usgs.gov/fdsnws/event/1/#parameters

## Techstack
* SQL
* Python
* PySpark
* Microsoft Fabric Services
  * **Data Factory** – Orchestration & ingestion (API, pipelines)
  * **Data Engineering (Notebooks&Spark)** – Transformations & Medallion architecture (Bronze/Silver/Gold)  
  * **OneLake (Lakehouse)** – Unified, scalable data lake storage  
  * **Data Warehouse** – SQL-based analytics & reporting
  * **Power BI** – Business intelligence, dashboards & insights
  * **Microsoft Entra ID** – Security, access management & RBAC

## Overview
### 1. Data Ingestion (Extraction)
* Connected to USGS API using Data Factory pipelines.
* Ingested raw data directly into OneLake (Lakehouse – Bronze layer).

### 2. Medallion Architecture (Transformation)
* Used Fabric notebooks (Spark) to process and clean data.
* Followed the Medallion architecture:
 * **Bronze** - Raw API data
 * **Silver** - Cleaned & Structured data
 * **Gold** - Aggregated, business-ready tables
* Scheduled pipelines to automate ingestion + notebook execution, ensuring reproducibility.

### 3. Final Data for Analysis (Load)
* Data is structured into Star Schema models (Gold Layer) within the Lakehouse for analytics and reporting.
* Curated data is made available in the Fabric Data Warehouse for optimized querying.
* Power BI connects directly to the Gold Layer/Data Warehouse for interactive, real-time dashboards and insights.

### 4. PowerBI Report
<img width="975" height="472" alt="image" src="https://github.com/user-attachments/assets/cb2f12ea-21fa-4ab5-8437-8c2dd0dc7aed" />

## Key Learnings
* Gained hands-on experience building an end-to-end ETL pipeline in Microsoft Fabric using parameterized pipelines and notebooks.
* Learned how to design incremental data ingestion by configuring pipelines to fetch only new daily records, reducing cost and improving efficiency.
* Strengthened skills in data transformation and validation within notebooks before loading into the Lakehouse.
* Developed a Power BI geospatial visualization (map with bubble markers) to represent earthquake event frequency and magnitude, improving storytelling with data.
* Practiced automation and scheduling by setting up a daily pipeline trigger for continuous data refresh.
* Understood the importance of data model design for reporting (choosing the right schema to support analysis).
* Enhanced knowledge of integrating external APIs (USGS) with Fabric pipelines for real-world data scenarios.
