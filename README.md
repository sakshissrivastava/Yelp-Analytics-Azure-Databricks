# Yelp Analytics with Azure Databricks

A comprehensive data analytics solution leveraging Azure cloud services to analyze Yelp's business reviews dataset using PySpark and advanced data formats.

## Project Overview

This project demonstrates end-to-end ETL pipeline implementation using Azure Databricks to analyze the Yelp reviews dataset. The solution processes multiple data sources including business information, check-ins, reviews, tips, and user data to extract meaningful business insights.

## Technical Architecture

### Storage Layer
- **Azure Data Lake Storage (ADLS):** For raw data management.
- **Parquet Format:** Used for optimized analytical queries.
- **Delta Lake:** Implemented for ACID transaction support.

### Processing Layer
- **Azure Databricks:** Utilized for distributed computing.
- **PySpark:** For large-scale data transformations.
- **Azure Data Factory:** For pipeline orchestration.

## Implementation Details

### Data Pipeline Steps

####Sample data ingestion
```python`
df_business = spark.read.json("abfss://sourcecontainer@sgyelp.dfs.core.windows.net/business.json")df_business.write.mode('overwrite').parquet("business.parquet")```

### Key Analytics Features
- User behavior analysis through review patterns.
- Business performance metrics and rankings.
- Geographic distribution studies.
- Restaurant performance analysis.
- Category-wise insights.

## Analysis Components

### Business Intelligence
- Identification of top performers across categories.
- User engagement metrics and fan base analysis.
- Review pattern analysis.
- Geographic performance insights.
- Restaurant ranking system.

### Performance Optimizations
- JSON to Parquet conversion for query optimization.
- Strategic data partitioning.
- Broadcast joins implementation.
- Delta format for better data management.

## Tech Stack

| Component            | Details                                    |
|----------------------|--------------------------------------------|
| **Language**         | Python3                                   |
| **Services**         | Azure Data Factory, Azure Databricks, ADLS|
| **Data Formats**     | JSON, Parquet, Delta Lake                 |

## Usage Instructions

1. Download the Yelp academic dataset containing business, check-in, review, tips, and user data.
2. Create an Azure resource manager and storage account.
3. Set up containers in Azure Storage for dataset upload.
4. Use Azure Data Factory to create pipelines for data movement into ADLS.
5. Configure Databricks workspace and cluster for processing the dataset.
6. Convert JSON files into Parquet/Delta formats for optimized analytics.
7. Perform analysis using Spark DataFrames in Databricks.

## Results and Impact

This project showcases enterprise-level data engineering practices while providing actionable business insights through modern cloud technologies. The analysis includes:
- Top-rated businesses by state and category.
- User engagement trends based on reviews and fan counts.
- Insights into geographic distributions of businesses.


![image](https://user-images.githubusercontent.com/70576003/199231783-c611e6d2-9cf1-4431-85e9-9c048f478b3a.png)  

![image](https://user-images.githubusercontent.com/70576003/199230927-96d39eac-451c-4e75-8d3f-d3ec80120350.png)  

![image](https://user-images.githubusercontent.com/70576003/199231043-2433de8c-ab77-4c47-9455-6da7cd88e0eb.png)


