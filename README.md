# Amazon_Sales_Analysis# Amazon_Sales_Analysis
## End-to-End Data Engineering & ML Pipeline

## Azure Databricks | Microsoft Fabric | Power BI

---

## Project Overview

This project demonstrates a complete data engineering and analytics pipeline built using Azure Databricks, Microsoft Fabric, and Power BI.

The goal of the project is to:

* Process Amazon sales datasets (2022 vs 2023)
* Detect statistical changes (data drift)
* Apply machine learning models
* Build an interactive dashboard for business insights

The project follows a modern Medallion Architecture (Bronze → Silver → Gold) and represents a real-world data pipeline design.

---

## Architecture Overview

* ADLS (Raw Data)
* Databricks – Bronze Layer (Data Ingestion)
* Databricks – Silver Layer (Cleaning and Transformation)
* Databricks – Gold Layer (Statistical Analysis and Machine Learning)
* Microsoft Fabric Pipeline (Orchestration)
* SQL Warehouse / Lakehouse
* Power BI Dashboard (Visualization)

---

## Medallion Architecture

### Bronze Layer (Raw Data)

* Data is ingested from Azure Data Lake Storage (ADLS)
* Stored in raw format without transformation
* Incremental loading implemented using sliding window approach

---

### Silver Layer (Cleaned Data)

* Data cleaning and preprocessing performed
* Missing values handled
* Schema corrected and data types standardized
* Feature engineering applied
* Data stored using Unity Catalog

---

### Gold Layer (Analytics and ML Ready)

#### Gold_Stats (Statistical Analysis)

* Mean (Average Revenue)
* Standard Deviation
* Skewness and Kurtosis
* Data Drift Detection
* Hypothesis Testing using p-value

#### Gold_ML (Machine Learning)

* Models used:

  * Linear Regression
  * Decision Tree
  * Random Forest
* Performance evaluated using R² score
* Comparison between:

  * Current dataset (2023)
  * Previous dataset (2022)

---

## Tech Stack

| Category        | Tools Used                     |
| --------------- | ------------------------------ |
| Cloud Storage   | Azure Data Lake Storage (ADLS) |
| Data Processing | Azure Databricks               |
| Language        | PySpark, Python                |
| Data Governance | Unity Catalog                  |
| Orchestration   | Microsoft Fabric Pipeline      |
| Data Serving    | SQL Warehouse / Lakehouse      |
| Visualization   | Power BI                       |

---

## Pipeline Workflow

### Data Ingestion

* Load raw data from ADLS into Bronze layer
* Apply sliding window for incremental updates

### Data Transformation

* Clean and structure data in Silver layer
* Apply transformations and feature engineering

### Statistical Analysis

* Compute statistical metrics
* Identify data drift between datasets

### Machine Learning

* Train models on both datasets
* Compare performance using R² score

### Orchestration

* Automate pipeline using Microsoft Fabric
* Manage dependencies from Bronze → Silver → Gold

### Visualization

* Connect SQL Warehouse to Power BI
* Build dashboard for insights

---

## Dashboard Insights

### Model Performance

* Comparison of R² scores across models and datasets

### Revenue Analysis

* Mean, variance, and distribution of revenue

### Data Drift Detection

* Changes in skewness and kurtosis

### Correlation Analysis

* Relationship changes between features

---

## Machine Learning Insights

* Random Forest and Decision Tree perform better than Linear Regression
* Previous dataset shows higher R², indicating possible overfitting or stable patterns
* Current dataset shows more variability, reflecting real-world changes

---

## Statistical Insights

* Increase in average revenue from 2022 to 2023
* Higher standard deviation indicates increased variability
* Changes in skewness and kurtosis suggest distribution shift
* P-value close to zero indicates statistically significant difference

Conclusion: Data drift is present between the datasets

---

## Project Structure

* Bronze_ingestion

  * Handles raw data ingestion

* Silver_cleaning

  * Performs data cleaning and transformation

* Gold_Stats

  * Performs statistical analysis

* Gold_ML

  * Builds and evaluates machine learning models

* utils

  * Contains reusable utility functions

* data/

  * Stores input datasets

* pipeline/

  * Contains Fabric pipeline configurations

* dashboard/

  * Power BI dashboard files

* README.md

  * Project documentation

---

## How to Run the Project

* Upload datasets to Azure Data Lake Storage
* Open Databricks workspace
* Execute notebooks in sequence:

  * Bronze → Silver → Gold
* Configure Microsoft Fabric pipeline
* Connect processed data to SQL Warehouse
* Build and view dashboard in Power BI

---

## Key Features

* End-to-end data pipeline implementation
* Medallion architecture design
* Incremental data processing using sliding window
* Combined statistical and machine learning analysis
* Automated pipeline orchestration
* Business-focused dashboard creation

---
  



