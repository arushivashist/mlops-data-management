# MLOps Data Management Project

This repository showcases a comprehensive MLOps workflow focused on data pipeline creation, feature engineering, and feature store management using tools like Apache Airflow, Docker, Feast, and AWS.

## Repo Overview

1. **Data Pipeline Development**: Building a data pipeline using Apache Airflow to:
   - Download raw data from Kaggle.
   - Perform feature engineering.
   - Convert data into various formats.
   - Commit and version data using Git and DVC.

2. **Feature Store Implementation**: Utilizing Feast to:
   - Create a feature repository.
   - Manage feature views.
   - Query the feature store for historical data.

3. **Cloud and Virtualization Integration**:
   - AWS S3 for data storage.
   - Docker for containerized workflow execution.
   - Virtual Machine setup for workflow orchestration.

## Key Components

### Data Pipeline with Apache Airflow

1. **Dataset Handling**:
   - Download raw datasets using the Kaggle CLI.
   - Process datasets to add engineered features (e.g., `TotalAddonServices`, `AvgMonthlyUsage`, `TenureGroup`).
   - Convert processed data into Parquet format.

2. **Versioning with Git and DVC**:
   - Set up Git and DVC repositories.
   - Push transformed datasets and Parquet files to version control.

3. **DAG Setup**:
   - Automated the entire data pipeline as a Directed Acyclic Graph (DAG) using Apache Airflow.
   - Tasks executed within the DAG:
     - Downloading datasets.
     - Transforming data.
     - Converting formats.
     - Committing and pushing files to Git/DVC.

### Feature Store with Feast

1. **Feature Repository Setup**:
   - Created and initialized a Feast feature repository.
   - Defined feature views using the transformed data.

2. **Feature Retrieval**:
   - Queried the feature store for historical data using `get_historical_features`.
   - Prepared data for downstream tasks like model training.

3. **Data Augmentation**:
   - Added timestamps to enable feature management in Feast.
   - Ensured compatibility with Feast's data ingestion pipeline.

### Cloud and Virtual Machine Setup

1. **AWS Integration**:
   - Utilized an S3 bucket for storing and managing datasets.

2. **Docker**:
   - Deployed Airflow components (scheduler, web server) via Docker Compose.

3. **VM Configuration**:
   - Set up a virtual machine on AWS using Ubuntu for seamless orchestration.
   - Configured secure access using SSH.

## Tools and Technologies

- **Workflow Orchestration**: Apache Airflow
- **Feature Store**: Feast
- **Version Control**: Git, DVC
- **Cloud Services**: AWS S3, EC2
- **Containerization**: Docker
- **Programming Languages**: Python
- **APIs**: Kaggle API

