# DuckDB Star Wars Analytics

Explore analytical SQL capabilities with DuckDB using Star Wars universe data.

## What You'll Learn

- In-memory analytical database operations
- SQL aggregations and grouping
- JOIN operations between tables
- Data export to Parquet format
- Direct Parquet file querying

## Prerequisites

- Python 3.8+
- Jupyter Notebook
- `duckdb` Python package

## Setup

1. **Install dependencies:**
   ```bash
   pip install duckdb jupyter
   ```

2. **Open the notebook:**
   ```bash
   jupyter notebook star_wars_analytics.ipynb
   ```

## Lab Contents

The notebook demonstrates:

1. **Database Connection** - Create in-memory DuckDB instance
2. **Table Creation** - Set up characters and planets tables
3. **Data Seeding** - Insert Star Wars character and planet data
4. **Basic Queries** - SELECT, WHERE, ORDER BY operations
5. **Aggregations** - GROUP BY and analytical functions
6. **JOIN Operations** - Combine character and planet data
7. **Parquet Export** - Save query results to files
8. **File Querying** - Query Parquet files directly

## Key DuckDB Features

- **In-memory processing**: Fast analytical queries
- **SQL compatibility**: Standard SQL with extensions
- **Parquet integration**: Native support for columnar format
- **Zero configuration**: No server setup required
- **Python integration**: Easy embedding in applications

## Sample Data

- **Characters**: 7 iconic Star Wars characters with affiliations and midichlorian counts
- **Planets**: 7 planets with climate and region information
- **Relationships**: Characters linked to their homeworlds

## Output Files

The lab generates:
- `jedi.parquet`: Jedi characters data
- `characters_with_planets.parquet`: Enriched character information