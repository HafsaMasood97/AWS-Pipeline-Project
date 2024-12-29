# YouTube Data Insights Pipeline

## Overview
This project is focused on securely managing, processing, and analyzing YouTube video data to derive insights based on video categories, trending metrics, and other key statistics. By leveraging AWS cloud services, the project aims to create an efficient, scalable system for ingesting, transforming, and visualizing YouTube data.

## Project Goals
- **Data Ingestion**: Build a mechanism to collect and ingest data from YouTube or external datasets.
- **ETL Process**: Process and transform the raw data into a structured format for analysis using AWS tools.
- **Data Lake**: Store raw and processed data in Amazon S3, providing a centralized repository.
- **Scalability**: Ensure that the system can scale to accommodate large datasets and handle increasing traffic.
- **Cloud Integration**: Leverage the power of AWS to perform data processing and visualization without the need for local computing resources.
- **Reporting & Dashboards**: Build interactive and dynamic dashboards using Amazon QuickSight to visualize the insights derived from the data.

## AWS Services and Tools Used
- **Amazon S3**: Cloud storage service used to store raw and processed datasets.
- **AWS IAM**: Manages user access to AWS resources securely.
- **AWS Glue**: Serverless data integration service to transform and prepare data for analysis.
- **AWS Lambda**: Serverless computing service for running code in response to events without managing servers.
- **AWS Athena**: Interactive query service to analyze data directly in Amazon S3 using SQL queries.
- **Amazon QuickSight**: A cloud-powered business intelligence service used for creating dashboards and visualizing data trends.

## Dataset Used
The project uses the YouTube New Dataset available on Kaggle. This dataset includes daily statistics of trending YouTube videos across various regions. Data fields include:

- Video title
- Channel title
- Publication time
- Tags
- Views, likes, dislikes
- Description
- Comment count
- Category_id (varies by region)

You can access the dataset here: [YouTube New Dataset on Kaggle](https://www.kaggle.com/datasets/)

## Architecture
The architecture of the project leverages multiple AWS services for data ingestion, processing, and reporting. The key components of the system are as follows:

- **Data Ingestion**: Data is either manually uploaded to Amazon S3 or fetched from APIs, depending on your setup.
- **ETL Process**: The raw data is processed and cleaned using AWS Glue, where we extract, transform, and load the data into a structured format suitable for analysis.
- **Data Storage**: The processed data is stored in Amazon S3, enabling quick access and management.
- **Data Analysis**: AWS Athena is used to perform SQL queries directly on data stored in S3, making data analysis more efficient and cost-effective.

## Architecture Diagram
![Architecture Diagram](Architecture%20diagram.png)

## Visualization
Amazon QuickSight is used to build dashboards and reports. It connects to Athena and S3, enabling you to visualize the results of your queries. QuickSight can help create visualizations such as:
- Video performance over time
- Trends by category
- Top-performing channels

![QuickSight Dashboard](Quicksight%20dashboard.png)
