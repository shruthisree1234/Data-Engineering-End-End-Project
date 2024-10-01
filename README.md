# Data-Engineering-End-End-Project

**Data Platform Architecture**
SoftCart uses a hybrid architecture, with some of its databases on premises and some on cloud.

Tools and Technologies:
OLTP database - MySQL
NoSql database - MongoDB
Production Data warehouse – DB2 on Cloud
Staging Data warehouse – PostgreSQL
Big data platform - Hadoop
Big data analytics platform – Spark
Business Intelligence Dashboard - IBM Cognos Analytics
Data Pipelines - Apache Airflow
Process:
SoftCart's online presence is primarily through its website, which customers access using a variety of devices like laptops, mobiles and tablets.

All the catalog data of the products is stored in the MongoDB NoSQL server.

All the transactional data like inventory and sales are stored in the MySQL database server.

SoftCart's webserver is driven entirely by these two databases.

Data is periodically extracted from these two databases and put into the staging data warehouse running on PostgreSQL.

The production data warehouse is on the cloud instance of IBM DB2 server.

BI teams connect to the IBM DB2 for operational dashboard creation. IBM Cognos Analytics is used to create dashboards.

SoftCart uses Hadoop cluster as its big data platform where all the data is collected for analytics purposes.

Spark is used to analyse the data on the Hadoop cluster.

To move data between OLTP, NoSQL and the data warehouse, ETL pipelines are used and these run on Apache Airflow.

**TASKS**
1) OLTP DATABASE DESIGN (https://author-ide.skills.network/render?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJtZF9pbnN0cnVjdGlvbnNfdXJsIjoiaHR0cHM6Ly9jZi1jb3Vyc2VzLWRhdGEuczMudXMuY2xvdWQtb2JqZWN0LXN0b3JhZ2UuYXBwZG9tYWluLmNsb3VkL0lCTS1EQjAzMjFFTi1Ta2lsbHNOZXR3b3JrL29sdHAvb2x0cC5tZCIsInRvb2xfdHlwZSI6InRoZWlhZG9ja2VyIiwiYWRtaW4iOmZhbHNlLCJpYXQiOjE3MjE3MzIwNjF9.hXrXgJHu-o_zEzqKjuplbKsWcgGSzA3voLx2nSlN5gs)
design the schema for OLTP database.
load data into OLTP database.
automate admin tasks.

2) Querying Data in NoSQL Databases (https://author-ide.skills.network/render?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJtZF9pbnN0cnVjdGlvbnNfdXJsIjoiaHR0cHM6Ly9jZi1jb3Vyc2VzLWRhdGEuczMudXMuY2xvdWQtb2JqZWN0LXN0b3JhZ2UuYXBwZG9tYWluLmNsb3VkL0lCTS1EQjAzMjFFTi1Ta2lsbHNOZXR3b3JrL25vc3FsL25vc3FsLm1kIiwidG9vbF90eXBlIjoidGhlaWFkb2NrZXIiLCJhZG1pbiI6ZmFsc2UsImlhdCI6MTcyMTczMjM0NH0.IWeHOVWkC29UHIDb1qToMJ5n6s4lNtoPqziIZHrjg04)
import data into a MongoDB database.
query data in a MongoDB database.
export data from MongoDB.

3) DATA WAREHOUSE DESIGN AND SETUP (https://author-ide.skills.network/render?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJtZF9pbnN0cnVjdGlvbnNfdXJsIjoiaHR0cHM6Ly9jZi1jb3Vyc2VzLWRhdGEuczMudXMuY2xvdWQtb2JqZWN0LXN0b3JhZ2UuYXBwZG9tYWluLmNsb3VkL0lCTS1EQjAzMjFFTi1Ta2lsbHNOZXR3b3JrL2RhdGF3YXJlaG91c2luZy9kdy5tZCIsInRvb2xfdHlwZSI6InRoZWlhb3BlbnNoaWZ0IiwiYWRtaW4iOmZhbHNlLCJpYXQiOjE3MjE3MzI1MTJ9.1vUpiQ3RvsKx921mXLxyDbtBsnSbc2CXkbJ3v78w5NQ)
Design a Data Warehouse using the pgAdmin ERD design tool.
Create the schema in the Data Warehouse

4) DATA WAREHOUSE REPORTING (https://author-ide.skills.network/render?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJtZF9pbnN0cnVjdGlvbnNfdXJsIjoiaHR0cHM6Ly9jZi1jb3Vyc2VzLWRhdGEuczMudXMuY2xvdWQtb2JqZWN0LXN0b3JhZ2UuYXBwZG9tYWluLmNsb3VkL0lCTS1EQjAzMjFFTi1Ta2lsbHNOZXR3b3JrL2RhdGF3YXJlaG91c2luZy9GaW5hbF9Bc3NpZ25tZW50X3dpdGhfcG9zdGdyZXMubWQiLCJ0b29sX3R5cGUiOiJ0aGVpYWRvY2tlciIsImFkbWluIjpmYWxzZSwiaWF0IjoxNzIyODYwMzA5fQ.N_R9VzphLyvrxHofNLSG_Z0qsNBScfXqObb0AnL6exU)
Load data into Data Warehouse
Write aggregation queries
Create MQTs

5) DASHBOARD CREATION (https://author-ide.skills.network/render?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJtZF9pbnN0cnVjdGlvbnNfdXJsIjoiaHR0cHM6Ly9jZi1jb3Vyc2VzLWRhdGEuczMudXMuY2xvdWQtb2JqZWN0LXN0b3JhZ2UuYXBwZG9tYWluLmNsb3VkL2lobmE3MGRtVy1uRF9mWmhGQXktc0EvYW5hbHl0aWNzLWxvb2tlci12MS5tZCIsInRvb2xfdHlwZSI6Imluc3RydWN0aW9uYWwtbGFiIiwiYWRtaW4iOmZhbHNlLCJpYXQiOjE3MTU2NzEzMDV9._UyJB7S4xNVA0WFTaQjF9pQUMd3AfDgcfWTDB2zYULk)
Create a dashboard using Google Looker Studio

6) SYNCING (https://author-ide.skills.network/render?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJtZF9pbnN0cnVjdGlvbnNfdXJsIjoiaHR0cHM6Ly9jZi1jb3Vyc2VzLWRhdGEuczMudXMuY2xvdWQtb2JqZWN0LXN0b3JhZ2UuYXBwZG9tYWluLmNsb3VkL0lCTS1EQjAzMjFFTi1Ta2lsbHNOZXR3b3JrL0VUTC9FVEwubWQiLCJ0b29sX3R5cGUiOiJ0aGVpYWRvY2tlciIsImFkbWluIjpmYWxzZSwiaWF0IjoxNzIyODY4MDc4fQ.DknImZE4AjbEuLtb5ytz3mxkXgBRPZx9hVc6w8ZsaiY)
One task that is routinely performed is the sync up of staging data warehouse and production data warehouse. Automating this sync up will save you a lot of time and standardize your process. You will be given a set of python scripts to start with. You will use/modify them to perform the incremental data load from MySQL server which acts as a staging warehouse to the IBM DB2 or PostgreSQL which is a production data warehouse. This script will be scheduled by the data engineers to sync up the data between the staging and production data warehouse.

7) Data Pipelines Using Apache AirFlow (https://author-ide.skills.network/render?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJtZF9pbnN0cnVjdGlvbnNfdXJsIjoiaHR0cHM6Ly9jZi1jb3Vyc2VzLWRhdGEuczMudXMuY2xvdWQtb2JqZWN0LXN0b3JhZ2UuYXBwZG9tYWluLmNsb3VkL0lCTS1EQjAzMjFFTi1Ta2lsbHNOZXR3b3JrL0VUTC9EYXRhX3BpcGVsaW5lc191c2luZ19haXJmbG93Lm1kIiwidG9vbF90eXBlIjoidGhlaWFkb2NrZXIiLCJhZG1pbiI6ZmFsc2UsImlhdCI6MTcyMTczNDg0M30.UCx5UbqwRUY4xxao1P8AWcmri7h6EMrat50RpXrD2nM)
Extract data from a web server log file
Transform the data
Load the transformed data into a tar file

8) SPARK MLOPS
