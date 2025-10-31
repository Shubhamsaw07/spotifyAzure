# spotifyAzure

##  Spotify End-to-End Azure Data Engineering Project

###  Overview
This project demonstrates a complete **end-to-end data engineering pipeline** built using **Azure** and **Databricks**, following the **Medallion Architecture (Bronze–Silver–Gold)**.  
The system processes and transforms Spotify data (users, artists, tracks, and analytics) from raw ingestion to clean, analytics-ready datasets for business insights.

### Project Architecture Breakdown

####  1. Data Ingestion (Bronze Layer)
Source Systems:
   Azure SQL Database (structured data)  
   GitHub API / CSV / JSON files (semi-structured data)
   Technology:Azure Data Factory (ADF)
   Purpose: 
   Extract raw Spotify data and load it into Azure Data Lake Storage (ADLS Gen2).
Output: 
  Raw unprocessed data stored in the Bronze layer.

#### 2. Data Transformation (Silver Layer)
Technology: Databricks (PySpark + Delta Live Tables)
Purpose: 
   Clean, standardize, and enrich raw data  
   Handle schema drift, nulls, and duplicates  
   Build dimension tables ('DimUser', 'DimArtist', 'DimTrack','DimDate','FactStream')
Output:  
  Curated and validated data stored in the Silver layer.

#### 3. Data Aggregation (Gold Layer)
Technology: Databricks + Delta Tables
Purpose:  
   Join and aggregate data into fact tables  
   Compute KPIs such as Top Artists by Country, Daily Stream Counts, etc.  
   Optimize tables for reporting and BI tools.
   Output: 
  Aggregated, analytics-ready data stored in the Gold layer.



| Layer         | Tools / Services                                   |
|---------------|----------------------------------------------------|
| Ingestion     | Azure Data Factory, Azure SQL Database             |
| Storage       | Azure Data Lake Gen2                               |
| Processing    | Databricks, PySpark, Delta Live Tables             |
| Orchestration | Azure Data Factory, Databricks Jobs                |
| Governance    | Unity Catalog, Azure Key Vault, Azure Entra ID     |
| CI/CD         | DataBricks Asset Bundle, GitHub                    |

  

  


