# Azure Medallion DBT DF ADB Project


This project demonstrates the implementation of a Medallion Architecture using various Azure services such as Azure Data Factory (ADF), Azure SQL Database, Azure Data Lake Gen2, Azure Databricks, and dbt (data build tool). The architecture facilitates the extraction, transformation, and loading (ETL) process, enabling the creation of curated data sets for analytical purposes.

## Overview

The Medallion Architecture divides data into three layers: Bronze, Silver, and Gold. In this project, we utilize Azure services to migrate data from Azure SQL Database to Azure Data Lake Gen2 in the Bronze layer using Azure Data Factory. Subsequently, the data is transformed and copied from the Bronze to the Silver layer in delta format using Azure Databricks. Finally, dbt is employed to perform transformations and create data marts, which are written to the Gold layer of the Data Lake Gen2.

## Architecture Components

- **Azure Data Factory (ADF):** Used for orchestrating and automating data movement and data transformation workflows.
- **Azure SQL Database:** The source database from which data is extracted.
- **Azure Data Lake Gen2:** Serves as the storage repository for data in the Medallion Architecture, with separate layers for Bronze, Silver, and Gold.
- **Azure Databricks:** Provides a unified analytics platform for big data and machine learning. Used here for data transformation tasks.
- **dbt (data build tool):** A tool that enables data analysts and engineers to transform data in their warehouse more effectively.

## Prerequisites

- Access to Azure services (Azure Data Factory, Azure SQL Database, Azure Data Lake Gen2, Azure Databricks).
- Python environment with dbt installed.

## Setup Instructions

1. **Azure Setup:** Ensure you have provisioned the necessary Azure services, including Data Factory, Data Lake Gen2, SQL Database, and Databricks. Configure appropriate access permissions.
2. **Data Migration:** Use Azure Data Factory to migrate data from the Azure SQL Database to the Bronze layer of the Azure Data Lake Gen2.
3. **Data Transformation:** Mount the Data Lake Gen2 to Azure Databricks and write scripts to copy data from the Bronze layer to the Silver layer in delta format.
4. **dbt Installation:** Install dbt in your local Python environment (virtual environment recommended).
5. **dbt Configuration:** Connect Azure Databricks with dbt and configure transformations to generate data marts. Write the transformed data to the Gold layer of the Data Lake Gen2.

