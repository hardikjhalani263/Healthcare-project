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
