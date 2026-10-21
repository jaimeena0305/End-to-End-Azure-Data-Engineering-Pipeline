# Netflix Data Engineering Project | Azure, Databricks & PySpark

## Overview

This project demonstrates an end-to-end data engineering pipeline built using Microsoft Azure and Azure Databricks to process Netflix movies and TV shows data.

The pipeline follows the Medallion Architecture, organizing data into Bronze, Silver, and Gold layers. It uses Databricks Auto Loader for incremental data ingestion, PySpark for data transformation, Delta Lake for reliable storage, and Delta Live Tables (DLT) for building Gold-layer tables.

The objective is to transform raw Netflix datasets into structured, analytics-ready data while developing practical skills in cloud data engineering, incremental processing, and data pipeline design.

## Tech Stack

- **Cloud Platform:** Microsoft Azure
- **Data Processing:** Azure Databricks, Apache Spark, PySpark
- **Data Ingestion:** Databricks Auto Loader
- **Cloud Storage:** Azure Data Lake Storage Gen2 (ADLS Gen2)
- **Storage Format:** Delta Lake
- **Data Pipeline Architecture:** Medallion Architecture
- **Pipeline Development:** Delta Live Tables (DLT)
- **Data Format:** CSV and Delta tables
- **Programming Languages:** Python, SQL

## Architecture

The project follows the Medallion Architecture.

```text
              Netflix Dataset (CSV Files)
                         |
                         v
              Azure Data Lake Storage
                         |
                         v
                 BRONZE LAYER
              Raw / Incremental Data
                         |
                         v
                 SILVER LAYER
            Cleaned and Transformed Data
                         |
                         v
                  GOLD LAYER
            Curated Analytics-Ready Tables
                         |
                         v
              Downstream Data Analytics
