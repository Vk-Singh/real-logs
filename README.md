# Real-time Data Warehouse System

This project builds a production-grade real-time data warehouse capable of handling billions of records. It integrates open-source tools like Apache Kafka, Airflow, PostgreSQL, and Elasticsearch to support scalable data ingestion, processing, and indexing.

## Features

- **Free Kafka & Elasticsearch Clusters** – Set up using Docker Compose.
- **Airflow DAGs** – Modular ETL/ELT pipelines.
- **Real-time Log Indexing** – Ingest and index billions of events.
- **CI/CD Ready** – Supports automated deployments.
- **Schema Management** – Automates schema and table creation using custom operators.

## Tech Stack

- Apache Airflow
- Apache Kafka
- PostgreSQL
- Redis
- Superset (for BI dashboards)
- Apache Pinot (for real-time analytics)
- Elasticsearch
- Docker & Docker Compose

## Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/RealtimeDataWarehouse.git
cd RealtimeDataWarehouse
```

### 2. Set up environment variables

Configure your secrets in '.env'.

### 3. Launch the system

```bash
docker-compose up --build
```

This starts up Kafka, PostgreSQL, Redis, Airflow, and other services.

### 4. Access Services

- Airflow UI: [http://localhost:8080](http://localhost:8080)
- Superset UI: [http://localhost:8088](http://localhost:8088)
- Kafka UI: [http://localhost:9000](http://localhost:9000)

## Airflow DAGs

- `customer_dim_generator.py`: Generates dimension data for customers.
- `transaction_facts_generator.py`: Ingests transactional data.
- `schema_dag.py`: Ensures schemas exist in Pinot or other storage layers.
- `loader_dag.py`: Coordinates full ETL flow.

## Monitoring & Observability

- Logs can be shipped to Elasticsearch.
- Dashboards built in Superset or integrated with Grafana.

## CI/CD

Deployment workflows can be defined using GitHub Actions or similar CI/CD tools.

## License

MIT License
