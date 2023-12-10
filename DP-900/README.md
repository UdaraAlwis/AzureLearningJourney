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
    - Spark based data lakehouse with tabular abstraction
    - Data warehouse with fully relational SQL engine
- Data aggregated and loaded into an online analytical processing (OLAP)
- Data in data lake, data warehouse and analytical model can be queried

Data lakes - large scale data analytics, file based data processing

Data warehouse - store data in optimized relational schema

Data lakehouses  - data lakes with data warehouse capabilities

OLAP model - storage optimized for analyical workloads, drill up and down

Different types of users,

- Data Scientist - works with data files in data lake, explore and model data
- Data Analyst - query data in data warehouse
- Business User - consume pre-aggregated data in an OLAP, dashboard or report

### [Explore data roles and services](https://learn.microsoft.com/en-us/training/modules/explore-roles-responsibilities-world-of-data/)

- Database administrators - manage database, maintain, performance, optimization
- Data engineers - manage infrastructure, pipelines, transfer and transform data
- Data analysts - create visualizations, insights, analytical models

Data services,

- Azure SQL - SQL Database, SQL Managed Instance, SQL VM
- Azure Database for open source databases - MySQL, MariaDB, PostgresSQL
- Azure Cosmos DB - Global scale no-sql db. json, key-value pairs, column-families and graphs
- Azure Storage - Blob storage, file shares and tables
- Azure Data factory - Data pipelines to transfer and transform data,  used by data engineers to build extract, transform, and load (ETL) solution
- Azure Synapse Analytics - unified PaaS for Pipelines, SQL, Spark, KQL querying
- Azure Databricks - combines Apache Spark with SQL database semantics
- Azure HDInsight - Azure hosted clusters for open source big data processing, Apache Spark, Hadoop, HBase, Kafka
- Azure Stream Analytics - real time processing of data streams for analytics
- Azure Data Explorer - high performance querying of log and telemetry data, with Azure Synaps analytics (IOT)
- Microsoft Pureview - enterprise wide data governance and discoverability
- Microsoft Fabric - SaaS analytics platform for lakehouse

## LEARNING PATH 2: Explore relational data in Azure (DP-900) 

### [Explore fundamental relational data concepts](https://learn.microsoft.com/en-us/training/modules/explore-relational-data-offerings/)

### Understand relational data

Strucutred data with relationships

Diferent data types for columns

Most databases supports ANSI standard data types

### Understand normalization

Minimizes data duplication

- Each entity -> own table
- Atrributes -> into columns
- Row -> Unique Primary Key
- Relationships -> with Foreign keys


### Explore SQL

Structured Query Language: Microsoft SQL Server, MySQL, PostgreSQL, MariaDB, and Oracle

SELECT, INSERT, UPDATE, DELETE, CREATE, and DROP

Additional proprietary extensions,

- Transact-SQL by SQL Server database engine
- pgSQL used by PostgreSQL
- PL/SQL used by Oracle

### SQL statement types

- DDL - Data Definition Language (CREATE, ALTER, DROP, RENAME) - manage objects
- DCL - Data Control Language (GRANT, DENY, REVOKE) - manage access to objects
- DML - Data Manipulation Language (SELECT, INSERT, UPDATE, DELETE) - manipulate data 

### Describe database objects

- 1. View - Virtual table based on a select query (CREATE VIEW Deliveries)

- 2. Stored Proceedure - SQL statements that runs on command with parameters (CREATE PROCEDURE RenameProduct)

- 3. Index - Specifies a column in a table and create a copy of it in a sorted order with pointers to the rows (CREATE INDEX idx_ProductName)
- Helps quickly find in massive amount of data
- Creates a tree based structure for the query optimizer to use
- Consumes storage space
- Need to maintain the index according to changes you make to the data

### Azure SQL Services and Capabilities

- SQL Server on Azure VM - lift and shift features
- Azure SQL Managed instance (PaaS) - automated updates, back and maintenance (mutiple dbs)
- Azure SQL database (PaaS) - core capabilities of on-prem db (Single DB or Elastic Pool)
- Azure Edge - IOT workloads, for streaming time-series data

### Azure Services for Open-Source

- Azure Database for MySQL - based on community edition
- Azure Database for MariaDB -  based on community edition
- Azure Database for PosgreSQL - execute stored proceedures in db itself, pgsql, comes with PostgreSQL Flexible Server - more control and configurations

## LEARNING PATH 3: Explore non-relational data in Azure (DP-900) 

### [Explore Azure Storage for non-relational data](https://learn.microsoft.com/en-us/training/modules/explore-provision-deploy-non-relational-data-services-azure/)

### Azure Blob Storage

Store massive amounts of unstructured binary data, provides an API as well.

Azure Storage account provides blob containers to store the files.

Types of Blobs,

- Block blobs - optimized for infrequently changed files
- Page blobs - optimized for random read/write
- Append blobs - can only append data in small chunks

Access Tiers, (can migrate between as well)

- Hot - for frequently accessed data
- Cool - for infrequently accessed data (cheaper)
- Archive - used for historical data, takes long time to dehydrate (cheaper)


### Azure DataLake Storage Gen2

Intergrate into Azure Storage and can be used by Azure DataLake Store systems

Used with Hadoop in Azure HDInsight, Azure Databricks, Azure Synapse analytics

To activate, Enable Hierarchichal Namespace option in Azure Storage account 

### Azure Files

Cloud based network shares

Used in a Azure Storage account

100 TB in a single account and 1 TB in a single file

- Standard tier - with hard disk storage
- Premium tier - with sold state storage

Supported Network file protocols,
- Server Message Block (SMB) - compatible with mutiple operating systems
- Network File System (NFS) - for Linux and MacOs, uses a Premium tier

### Azure Tables

Used for storing semi-structured key-value data (Denormalized data)

Uses partitioning for grouping similar data for faster access, contains patition key and row key

### [Explore fundamentals of Azure Cosmos DB](https://learn.microsoft.com/en-us/training/modules/explore-non-relational-data-stores-azure/)

## Azure Cosmos DB

Fully managed and serverless

Fast read write performance and auto scaling 

For handling massive amounts of data

Provides an API to work with different data stores

Uses, 

- IoT and telematics. 
- Retail and Marketing
- Gaming
- Web and Mobile applications

APIs,

- Cosmos DB for NoSQL - uses JSON format, works with SQL syntax
- Cosmos DB for MongoDB - using Binary JSON and MQL query language
- Cosmos DB for PostgreSQL - native and scales upto multiple nodes
- Cosmos DB for Table - store data in key-value tables
- Cosmos DB for Apache Cassandra - uses column-family storage structure
- Cosmos DB for Apache Gremlin - uses graph data structure, nodes and edges

## LEARNING PATH 4: Explore data analytics in Azure (DP-900) 

### [Explore data analytics in Azure](https://learn.microsoft.com/en-us/training/paths/azure-data-fundamentals-explore-data-warehouse-analytics/)

### [Explore fundamentals of large-scale analytics](https://learn.microsoft.com/en-us/training/modules/examine-components-of-modern-data-warehouse/)

### Data warehousing architecture

Elements,

- Data ingestion and processing
    - Extract, Transform and Load (ETL)
    - Extract, Load and Transform (ELT)

- Analytical data store
    - data warehouse
    - data lakes

- Analytical data model
    - pre-aggregates the data for anlytics

- Data visualization
    - create reports and visulization

### Data injestion pipeline

Created using,

- Azure Data factory 
- Azure Synapse Analyitcs
- Microsoft Fabric

Pipelines that orchestrates ETL processes

### Analytical data stores

- Data warehouses - data stored in a schema optimized for analytics (structured data)
- Data lakehouses - data is stored in distributed file system optimized for fast access (semi-structured data)

### PaaS Solutions

Azure Synapse Analytics - high performance relationional data warehousing, easy User interface

Azure Databricks - build on Apache Spark, good for multi cloud environments

Azure HDInsight - for open-source data analytics clusters, not very user friendly

### Microsoft Fabric

SaaS with a single open format in OneLake

Single integrated environment


### [Explore fundamentals of real-time analytics](https://learn.microsoft.com/en-us/training/modules/explore-fundamentals-stream-processing/)


### Batch Processing

- Data is collected and stored, then processed together

- All the data must be ready before processing

- Problem with a data causes whole process to stop

### Stream Processing

- Data is constantly monitored and processed in real time

- Ideal for time-critical operations


Many large scale analytics solutions have both batch and stream processing included in their architecture

### Architecture for Stream processing

- data generated by sensors -> captured in a streaming source (queue processor) -> data is process by a query -> results pushed to a dashboard or further processing

### Real-time analytics in Azure

- Azure Stream Analytics - PaaS solution for streaming jobs
- Spark Structured Streaming - Open source, complex solutions with Azure Synapse Analytics, Azure Databricks, Azure HDInsight
- Azure Data Explorer - optimized for injesting and querying batch or streaming data

Sources (ingesting data) for Stream Processing

- Azure Event Hubs
- Azure IOT Hub
- Azure Data Lake Store Gen2 
- Apache Kafka

Sinks (output data) for Steam processing

- Azure Event Hubs
- Azure Data Lake Store Gen 2 / Azure Blog Storage
- Azure SQL Database, Synapse Analytics, Databricks
- Microsoft Power BI

### Azure Stream Analytics

Service for complex event processing and analysis of streaming data

Stream analytics query run perpetually as data arrives

Create a Stream Analytics job in Azure or a Stream Analysis cluster for complex tasks

### Apache Spark on Microsoft Azure

Distributed processing framework for large scale data anlytics

Used with,

- Azure Synapse Analytics
- Azure Databricks
- Azure HDInsight

Use Spark Structured Streaming API for ingestion, processing and outputting results from a data stream

### Delta Lake

Open source storage layer with support for transactional consistency, schema enforcement and other warehousing features

Azure Synapse Analytics and Azure Databricks include support for Delta Lake

### Realtime Analytics in Microsoft Fabric

Real time data anlytics and ingestion from multiple sources

Use an eventstream to capture real-time event data


### [Describe Power BI tools and workflow](https://learn.microsoft.com/en-us/training/modules/explore-fundamentals-data-visualization/2-power-bi)

Suite of tools and services for building interactive data visualizations

Import data into Power BI Desktop -> Power BI Service -> View the reports in Web browser or Phone App

### Core concepts of data modeling

- Dimentions - Entities to aggregate (Customer, Product)
- Measures - Numeric values to analyize 
- Facts - Numeric Measures to be aggregated 

Model forms a multi-dimentional structure (cube)

- Star schema - fact table is related to one or more dimension tables
- Snowflake schema - dimension tables are related to additional tables 

Attribute hierarchies - quickly drill-up and down for aggregated values

Data Visualizations,

- Tables and text
- Bar and Column charts
- Line Charts
- Pie Charts
- Scatter Plots
- Maps
- Interactive Reports in Power BI




