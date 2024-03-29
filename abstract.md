## Abstract

This project demonstrates building a cloud-based ETL pipeline for NYC Taxi data analysis. It implements best practices such as Infrastructure as Code (IaC), containerization, cloud infrastructure, and modern data stack.

The pipeline extracts the 2021-2022 NYC Yellow Taxi trip data files stored in a public S3 bucket as CSVs. These are loaded and transformed in Pandas locally before being uploaded to a Cloud Storage bucket. Postgres database and BigQuery data warehouse are leveraged with Docker containers to enable developing locally.

The data pipeline orchestration is handled by Apache Airflow, running in a Docker container, with workflows to partition, load, transform and validate the data. Infrastructure provisioning in GCP is automated using Terraform IaC. dbt handles the transformations for analytics in BigQuery. Several tests were also written to check the data quality. Looker provides business intelligence dashboards and reports for end users requiring insights.

The project demonstrates a reproducible, maintainable and production-grade cloud data engineering architecture using Docker, Terraform, Airflow, dbt, and Looker for ETL pipeline development. It follows best practices around testing, idempotency, and enviroment consistency. The dataset enables analysis for business use-cases like demand modeling.