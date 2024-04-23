# Currency Exchange Rate Data Pipeline

## Overview

The Currency Exchange Rate Data Pipeline is a comprehensive data pipeline built to automate the collection, processing, and analysis of currency exchange rates. The pipeline ensures the availability of the currency API and files, downloads the latest exchange rates, stores them in HDFS, creates a Hive table for querying, processes the data with Spark, and notifies stakeholders via email and Slack.

## Components

### Availability Checks

#### Currency API Check
- Verifies the availability of the currency exchange rates API by sending a request and checking for a successful response.

#### Currency File Check
- Ensures the availability of the currency exchange rates file by checking its existence in a specified location.

### Data Collection

#### Download Exchange Rates
- Fetches the latest exchange rates from the currency API upon successful availability checks.

### Data Storage

#### Save to HDFS
- Saves the downloaded exchange rates into HDFS, providing a scalable and fault-tolerant storage solution.

### Data Management

#### Create Hive Table
- Creates a Hive table to organize and structure the exchange rate data, enabling SQL-like querying capabilities.

### Data Processing

#### Process with Spark
- Processes the exchange rate data using Apache Spark, allowing for efficient and distributed data processing tasks like transformations, aggregations, and analytics.

### Notifications

#### Email Notification
- Sends email notifications upon successful completion of the pipeline or in case of any failures to notify stakeholders.

#### Slack Notification
- Sends Slack notifications to a designated channel to keep the team updated on the pipeline's status.

## Technologies Used

- **Apache Airflow:** For task orchestration and scheduling.
- **Apache Spark:** For data processing and analytics.
- **Hadoop HDFS:** For storing large datasets in a distributed manner.
- **Apache Hive:** For creating and querying structured data tables.
- **Python:** For scripting tasks and data manipulation.
- **APIs:** To fetch currency exchange rates from external sources.
