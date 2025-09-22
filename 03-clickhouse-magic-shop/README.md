# ClickHouse Magic Shop dbt Project

This is a dbt project demonstrating a star-schema data model for Ollivander & Co. Mail-Order Magic shop.

## Setup Instructions

1. **Start ClickHouse:**
   ```bash
   docker-compose up -d
   ```

2. **Create Databases:**
   Connect to ClickHouse and run:
   ```sql
   CREATE DATABASE IF NOT EXISTS raw;
   CREATE DATABASE IF NOT EXISTS analytics;
   ```

3. **Install dbt dependencies:**
   ```bash
   pip install dbt-core dbt-clickhouse
   ```

4. **Configure dbt profile:**
   Copy `profiles.yml` to `~/.dbt/profiles.yml` or set `DBT_PROFILES_DIR`

5. **Test connection:**
   ```bash
   cd magic_shop
   dbt debug
   ```

## Usage

1. **Load seed data:**
   ```bash
   dbt seed
   ```

2. **Run staging models:**
   ```bash
   dbt run --select staging
   ```

3. **Run marts:**
   ```bash
   dbt run --select marts
   ```

4. **Run tests:**
   ```bash
   dbt test
   ```

5. **Generate documentation:**
   ```bash
   dbt docs generate
   dbt docs serve
   ```

## Project Structure

- `seeds/`: Raw CSV data (customers, orders, payments)
- `models/staging/`: Clean, typed staging tables
- `models/marts/`: Dimensional model (dim_customers, fct_orders)
- `models/schema.yml`: Data quality tests

## Key Features

- **Incremental processing** for large fact tables
- **Data quality tests** to ensure integrity
- **ClickHouse optimizations** with proper engines and partitioning
- **Star schema design** for analytical queries