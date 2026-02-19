# spark-medallion-lakehouse-pipeline
Spark ETL pipeline implementing Bronze, Silver, and Gold layers to build a structured and analytics-ready data lakehouse.
Spark Medallion Lakehouse Pipeline

An end-to-end Spark-based ETL pipeline implementing the Medallion (Bronze–Silver–Gold) Lakehouse Architecture to transform raw data into analytics-ready datasets.

This project demonstrates how to design scalable data pipelines using Apache Spark while applying best practices in data layering, transformation, validation, and aggregation.

📌 Project Overview

Modern data platforms require structured pipelines that progressively improve data quality.
This project implements the Medallion Architecture, where data flows through three refinement layers:

🟤 Bronze Layer – Raw Ingestion

Stores raw source data (CSV/JSON)

Minimal transformation

Preserves original schema

Acts as immutable source of truth

⚪ Silver Layer – Cleaned & Transformed

Data cleaning & standardization

Null handling & schema enforcement

Deduplication & validation logic

Business-level transformations

🟡 Gold Layer – Analytics Ready

Aggregated datasets

Business KPIs

Optimized tables for reporting & BI tools

Star-schema–friendly outputs

This layered design ensures data reliability, reusability, and scalability.


🏛 Architecture Flow
Raw Source Data
       ↓
Bronze Layer (Raw Ingestion)
       ↓
Silver Layer (Cleaned & Validated Data)
       ↓
Gold Layer (Aggregated Business Metrics)

🛠 Technologies Used

Apache Spark (PySpark) – Distributed data processing

Python – ETL logic implementation

Parquet / CSV – Storage formats

Medallion Architecture – Data Lakehouse design pattern

Data Modeling Concepts – Aggregations & analytics datasets

📂 Project Structure
spark-medallion-lakehouse-pipeline/
│
├── raw_data/                # Raw input files (Bronze)
├── bronze/                  # Raw ingested layer
├── silver/                  # Cleaned & transformed layer
├── gold/                    # Aggregated analytics layer
├── scripts/                 # Spark ETL scripts
└── README.md
