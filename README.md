# Data Warehouse Project

Welcome to the **Data Warehouse Project** repository! 

This project demonstrates a comprehensive data warehousing solution, from building a data warehouse to generating actionable insights. 
 
---

## 📖 Project Overview

This project involves:

1. **Data Architecture**: Designing a Modern Data Warehouse Using Medallion Architecture **Bronze**, **Silver**, and **Gold** layers.
2. **ETL Pipelines**: Extracting, transforming, and loading data from source systems into the warehouse.
3. **Data Modeling**: Developing fact and dimension tables optimized for analytical queries.
 
---

## 🏗️ Data Architecture

The data architecture for this project follows Medallion Architecture **Bronze**, **Silver**, and **Gold** layers:
![Data Architecture](docs/architecture.png)

1. **Bronze Layer**: Stores raw data as-is from the source systems. Data is ingested from CSV Files into SQL Server Database.
2. **Silver Layer**: This layer includes data cleansing, standardization, and normalization processes to prepare data for analysis.
3. **Gold Layer**: Houses business-ready data modeled into a star schema required for reporting and analytics.

---

## 📝 Project Requirements

### ⚒️ Building the Data Warehouse (Data Engineering)

#### Objective
Develop a modern data warehouse using SQL Server to consolidate sales data, enabling analytical reporting and informed decision-making.

#### Specifications
- **Data Sources**: Import data from two source systems (ERP and CRM) provided as CSV files.
- **Data Quality**: Cleanse and resolve data quality issues prior to analysis.
- **Integration**: Combine both sources into a single, user-friendly data model designed for analytical queries.
- **Scope**: Focus on the latest dataset only; historization of data is not required.
- **Documentation**: Provide clear documentation of the data model to support both business stakeholders and analytics teams.

---

## 🛠️ Important Links & Tools:

- **[Datasets](datasets/):** Access to the project dataset (csv files).
- **[SQL Server Express](https://www.microsoft.com/en-us/sql-server/sql-server-downloads):** Lightweight server for hosting your SQL database.
- **[SQL Server Management Studio (SSMS)](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16):** GUI for managing and interacting with databases.
- **[Git Repository](https://github.com/):** Set up a GitHub account and repository to manage, version, and collaborate on your code efficiently.
- **[DrawIO](https://www.drawio.com/):** Design data architecture, models, flows, and diagrams.

---
## 📂 Repository Structure

```
sql-data-warehouse-project
|
+---datasets                                  # Raw datasets used for the project (ERP and CRM data)
|   +---source_crm
|   |       cust_info.csv
|   |       prd_info.csv
|   |       sales_details.csv
|   |
|   \---source_erp
|           CUST_AZ12.csv
|           LOC_A101.csv
|           PX_CAT_G1V2.csv
|
+---docs                                     # Project documentation and architecture details
|       architecture.png                     # The project's architecture
|       datacatalog.md	                     # Catalog of datasets, including field descriptions and metadata              											 						  
|       data_flow.png                        # The data flow diagram
|       data_model.png                       # Data models (star schema)
|       integration_model.png                # How tables are related and integrated
|       naming_conventions.md                # Consistent naming guidelines for tables, columns, and files
|
+---scripts                                  # SQL scripts for ETL and transformations
|   |   init_database.sql                    # Script for creating database and schemas
|   |
|   +---bronze_layer                         # Scripts for extracting and loading raw data
|   |       bronze_ddl.sql                   # Script creates tables in the bronze schema
|   |       proc_load_bronze.sql             # Stored procedure script loads data into the bronze schema
|   |
|   +---gold_layer                           # Scripts for creating analytical models
|   |       gold_ddl.sql                     # Script creates views for the Gold Layer in the data warehouse
|   |
|   \---silver_layer                         # Scripts for cleaning and transforming data
|           proc_load_silver.sql             # Stored procedure performs the ETL process to populate the silver schema tables from the bronze schema
|           silver_layer_ddl.sql             # Script creates tables in the silver schema
|
\---tests                                    # Test scripts and quality files
        quality_checks_gold.sql
        quality_checks_silver.sql
|
|   .gitignore                              # Files and directories to be ignored by Git
|   LICENSE                                 # License information for the repository
|   README.md                               # Project overview and instructions
```

---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE). You are free to use, modify, and share this project with proper attribution.

## 🌟 About Me

I am studying for Bachelor's degree in Business Information Technology at University of Applied Sciences and I will specialize in data. 
**To be continued...**
