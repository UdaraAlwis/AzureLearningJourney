# DP-900 Study Notes

DP-900 Exam guide: https://learn.microsoft.com/en-us/credentials/certifications/exams/dp-900/


LEARNING PATH 1: Microsoft Azure Data Fundamentals: Explore core data concepts


LEARNING PATH 2: Microsoft Azure Data Fundamentals: Explore relational data in Azure


LEARNING PATH 3: Microsoft Azure Data Fundamentals: Explore non-relational data in Azure


LEARNING PATH 4: Microsoft Azure Data Fundamentals: Explore data analytics in Azure


---


## LEARNING PATH 1: Explore core data concepts (DP-900) 

### [Explore core data concepts](https://learn.microsoft.com/en-us/training/paths/azure-data-fundamentals-explore-core-data-concepts/)

### Identify data formats

Structured Data - fixed schema, tabular, tables and columns with relational model

Semi-Structured Data - has some structure but allows certain variations

Unstructured Data - documents, images, audio/video/binary files, 

Data stores 
- File stores
- Databases

### Explore file storage

- Delimited text files - good for structured data
- JavaScript Object Notation (JSON) - good for structured and semi-structured data.
- Extensible Markup Language (XML)
- Binary Large Object (BLOB)

Optimized file formats

- Avro - row based data format, with a header description of structure
- ORC (Optimized Row Columnar format) - organize data into columns, stripes of data
- Parquet - columnar data format, row groups

### Explore databases

Relational databases - store and query structured data
Non-relational databases - 
    - Key-value databases
    - Document databases
    - Column-family databases
    - Graph databases


### Transactional data processing

A small descreet unit of work, often high volume

Online Transactional Processing (OLTP) solutions 

ACID semantics
- Atomicity - succeeds completely or fails complteley
- Consistency - one valid state to another
- Isolation - no concurrent interference
- Durability - committed data are persistent

### Analytical data processing

read only snapshot data at a given time or a series of snapshots


- Data Extracted, Transformed and Loaded (ETL) into Data lake
- Data loaded into a schema of tables, (two ways)
    > Spark based data lakehouse with tabular abstraction
    > Data warehouse with fully relational SQL engine
- Data aggregated and loaded into an online analytical processing (OLAP)
- Data in data lake, data warehouse and and analytical model can be queried

Data lakes - large scale data analytics, file based data processing

Data warehouse - store data in optimized relational schema

Data lakehouses  - data lakes with data warehouse capabilities

OLAP model - storage optimized for analyical workloads, drill up and down

Different types of users,

Data scientist - works with data files in data lake, explore and model data
Data analyst - query data in data warehouse
Business user - consume pre-aggregated data in an OLAP, dashboard or report

### [Explore data roles and services](https://learn.microsoft.com/en-us/training/modules/explore-roles-responsibilities-world-of-data/)

- Database administrators - manage database, maintain, performance, optimization
- Data engineers - manage infrastructure, pipelines, transfer and transform data
- Data analysts - create visualizations, insights, analytical models

Data services,

- Azure SQL - SQL Database, SQL Managed Instance, SQL VM
- Azure Database for open source databases - MySQL, MariaDB, PostgresSQL
- Azure Cosmos DB - global scale no-sql db. json, key-value pairs, column-families and graphs
- Azure Storage - blob storage, file shares and tables



## LEARNING PATH 2: Explore relational data in Azure (DP-900) 

### [Explore fundamental relational data concepts](https://learn.microsoft.com/en-us/training/modules/explore-relational-data-offerings/)






## LEARNING PATH 3: Explore non-relational data in Azure (DP-900) 

### [Explore Azure Storage for non-relational data](https://learn.microsoft.com/en-us/training/modules/explore-provision-deploy-non-relational-data-services-azure/)






## LEARNING PATH 4: Explore data analytics in Azure (DP-900) 

### [Explore data analytics in Azure](https://learn.microsoft.com/en-us/training/paths/azure-data-fundamentals-explore-data-warehouse-analytics/)


