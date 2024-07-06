# Snowflake
Snowflake related hands on project code

#Tesla Stock Project
Task Description:
This task is to create Snowflake tables and import Tesla Stock Data (a CSV file in AWS S3 Bucket) into Snowflake tables. After data has been successfully imported, we will use the AWS QuickSight to create reports on top of Snowflake tables. This data load can be done from Snowsight or SnowSQL, but we will focus on creating SnowSQL so that the code can be scheduled by job scheduler such as Control M.

Terminology
Staging Area: the intermediate place for the ELT. The most common method of loading data into Snowflake is to stage data into AWS S3 bucket, GCP cloud storage, or Azure blob storage, and from those files load data into the Snowflake.
Storage Integration in Snowflake: refers to the capability of Snowflake to integrate with external cloud storage platforms such as Amazon S3, Google Cloud Storage (GCS), or Microsoft Azure Blob Storage. This integration allows Snowflake to leverage the storage capabilities of these platforms to store and manage data that is stored externally to the Snowflake data warehouse.

Loading Steps
Create Target Table.
Create AWS IAM and Policies to allow Snowflake connect to AWS.
Create Storage Integration.
Create File Format & Stage.
Create Snow Pipe to Load data from Stage to Table (COPY INTO ... FROM ...).
Create Event Notification in AWS S3 bucket to trigger Snow Pipe job after file is present in S3 bucket. SHOW PIPE to gets pipe related SQL Queue Channel Information, then add that into event notification in AWS.
Create AWS QuickInsight Report.
Data & Code
https://github.com/pazhuo/Snowflake/blob/main/TSLA.csv
https://github.com/pazhuo/Snowflake/blob/main/TSLAmodified.csv
https://github.com/pazhuo/Snowflake/blob/main/Tesla_Stock_Data_AWSLoad.txt
https://github.com/pazhuo/Snowflake/blob/main/Tesla_Stock_Data_SnowSQL-Command.txt
