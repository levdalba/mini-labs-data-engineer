# Mini Labs: Data Engineering

A collection of hands-on data engineering mini-labs demonstrating key technologies and patterns used in modern data stacks.

## Labs Overview

### 1. Redis Coffee Shop Loyalty System (`01-redis-coffee-shop/`)

Learn Redis fundamentals by building a customer loyalty system for a coffee shop.

**Technologies:** Redis, Python  
**Concepts:** Key-value storage, counters, TTL (time-to-live), caching patterns

**What you'll build:**
- Customer registration and lookup
- Visit tracking with automatic counters  
- Temporary discount codes with expiration
- Complete loyalty workflow

**Getting Started:**
```bash
cd 01-redis-coffee-shop
docker-compose up -d
jupyter notebook coffee_loyalty_system.ipynb
```

### 2. DuckDB Star Wars Analytics (`02-duckdb-star-wars/`)

Explore analytical SQL with DuckDB using Star Wars character and planet data.

**Technologies:** DuckDB, Python  
**Concepts:** In-memory analytics, SQL aggregations, JOINs, Parquet export

**What you'll learn:**
- Fast in-memory analytical queries
- Data aggregation and grouping
- JOIN operations across tables
- Exporting results to Parquet format
- Querying Parquet files directly

**Getting Started:**
```bash
cd 02-duckdb-star-wars  
pip install duckdb
jupyter notebook star_wars_analytics.ipynb
```

### 3. ClickHouse Magic Shop (`03-clickhouse-magic-shop/`)

Build a complete ELT data pipeline using dbt and ClickHouse for a magical e-commerce store.

**Technologies:** ClickHouse, dbt, SQL  
**Concepts:** ELT pipelines, dimensional modeling, incremental processing, data quality testing

**What you'll build:**
- Seeds → Staging → Marts pipeline
- Star schema with dimensions and facts
- Incremental fact table processing
- Data quality tests and documentation
- ClickHouse-optimized table engines

**Getting Started:**
```bash
cd 03-clickhouse-magic-shop
docker-compose up -d
pip install dbt-core dbt-clickhouse
cd magic_shop
dbt debug
dbt seed
dbt run
dbt test
```

## Prerequisites

- Docker and Docker Compose
- Python 3.8+
- Jupyter Notebook
- Basic SQL knowledge

## Installation

Clone this repository:
```bash
git clone https://github.com/levdalba/mini-labs-data-engineer.git
cd mini-labs-data-engineer
```

Each lab has its own dependencies and setup instructions in its respective folder.

## Learning Path

1. **Start with Redis** to understand key-value stores and caching patterns
2. **Move to DuckDB** for analytical SQL and in-memory processing  
3. **Complete with ClickHouse/dbt** for production-scale data pipelines

## Technologies Covered

| Technology | Purpose | Lab |
|------------|---------|-----|
| Redis | Caching, session storage, real-time counters | Coffee Shop |
| DuckDB | Fast analytics, data exploration, prototyping | Star Wars |  
| ClickHouse | OLAP database, time-series data, large scale analytics | Magic Shop |
| dbt | Data transformation, testing, documentation | Magic Shop |
| Docker | Containerization, local development | All labs |
| Jupyter | Interactive development, data exploration | Redis, DuckDB |

## Next Steps

After completing these labs, you'll have hands-on experience with:
- NoSQL data stores (Redis)
- Analytical databases (DuckDB, ClickHouse)  
- Data transformation tools (dbt)
- Modern data stack patterns

Consider exploring:
- Apache Airflow for orchestration
- Apache Kafka for streaming
- Data visualization tools (Grafana, Metabase)
- Cloud data platforms (Snowflake, BigQuery, Databricks)