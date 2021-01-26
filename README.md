# Data Engineer Project - Syn transactional data to data warehouse for BI
- Create MySQL database instance on RDS as transactional database<br>
  - Connect DB client DBeaver to the transactional database on RDS<br>
  - Create tables and load data using DBeaver<br>
  - Data source: https://www.kaggle.com/olistbr/brazilian-ecommerce<br>
- Create a Data Warehouse in Redshift, and connect it to DBeaver<br>
- AWS DataPipeline: one-time load historical data into Redshift tables using copy command<br>
- AWS Glue: incremental data loads into Redshift <br>
  - use AWS Secret Managers to store credentials<br>
  - create a schema for staging tables in Redshift, and create staging tables<br>
  - copy current data from S3 and store into a staging table<br>
  - delete from the main table in the Data Warehouse using the staging tables<br>
  - insert into the main table in the Data Warehouse by selecting everything from the staging table, and truncate the staging table at the end of this process.<br>
  - use Lambda function to trigger the Glue job<br>
- Data Enrichment & Centralisation
   - User behaviour/Funnel data from external sources that is semi-structured can be stored in S3 (data lake)
   - use AWs Glue Crawler and Athena to read and query the data
   - 
  
