
# NYC Taxi Batch Data Engineering Pipeline (PySpark + Delta Lake + Databricks)

A complete **batch-only** data engineering project using **PySpark**, **Delta Lake**, and **Databricks**.

## 🏗️ Architecture
![Architecture](architecture.png)

```
Raw Files  →  Bronze (Raw)  →  Silver (Cleaned + Enriched)  →  Gold (Analytics & KPIs)
```

## 📁 Layers

### Bronze Layer
- Raw Parquet ingestion
- Metadata added: file_path, ingest_date, ingest_time

### Silver Layer
- Data cleaning, transformations, enrichments
- Zone lookup join
- Derived features: pickup_date, pickup_hour, trip_duration

### Gold Layer
- Daily KPIs
- Hourly KPIs
- Top pickup zones per day
- Revenue by borough
- Average fare trends

## 🚀 Technologies Used
- Databricks Community Edition
- PySpark
- Delta Lake
- Medallion Architecture

## 📊 Sample Outputs
Daily KPIs, revenue by borough, and fare trends are included in the project examples.

## 📦 Dataset
Yellow Taxi Trip Data:  
https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_2022-11.parquet  
https://d37ci6vzurychx.cloudfront.net/trip-data/yellow_tripdata_2022-12.parquet  

Taxi Zone Lookup:  
https://d37ci6vzurychx.cloudfront.net/misc/taxi_zone_lookup.csv

## ✔ Future Enhancements
- Add streaming ingestion (Kafka → Bronze)
- Add dashboards (PowerBI/Tableau)
- Add orchestration (Airflow / Databricks Jobs)

---

Created automatically for GitHub upload.
