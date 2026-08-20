# Healthcare-project
A production-style Healthcare Data Engineering project built on Azure Databricks using Unity Catalog, Delta Lake, and the Medallion Architecture (Bronze → Silver → Gold).

The project ingests multiple healthcare datasets, performs data cleansing and dimensional modeling, and creates analytics-ready Gold tables for reporting tools such as Power BI.

Project Overview

This project processes healthcare data from four different source files:

CMS Medicare Drug Spend (CSV)

CMS Hospital Cost Report FY2022 (CSV)

ICD-10 Diagnosis Reference (TXT)

Synthea FHIR Patient Data (JSON/CSV)

The pipeline stores raw data in the Bronze layer, transforms it into dimensional tables in the Silver layer, and creates business-ready analytical tables in the Gold layer.
<img width="958" height="500" alt="image" src="https://github.com/user-attachments/assets/023619d6-3fa8-49b3-8288-fcbe419c716e" />

healthcare_catalog

│

├── raw

│   └── healthcare_files (Volume)

│

├── bronze

│   ├── bronze_drug_spend

│   ├── bronze_hospital_cost

│   ├── bronze_icd10

│   └── bronze_fhir

│

├── silver

│   ├── dim_physician

│   ├── dim_drug

│   ├── dim_facility

│   ├── dim_diagnosis

│   ├── dim_date

│   └── fact_drug_spend

│

└── gold

    ├── gold_drug_analytics
    
    ├── gold_hospital_analytics
    
    └── gold_physician_performance

    Technologies Used

Azure Databricks

Unity Catalog

Delta Lake

PySpark

Spark SQL

Databricks Volumes

Git & GitHub

Project Workflow
Step 1 – Unity Catalog Setup

Created:

- Catalog
- Schemas
- Volume


CREATE CATALOG healthcare_catalog;

CREATE SCHEMA healthcare_catalog.raw;

CREATE SCHEMA healthcare_catalog.bronze;

CREATE SCHEMA healthcare_catalog.silver;

CREATE SCHEMA healthcare_catalog.gold;
