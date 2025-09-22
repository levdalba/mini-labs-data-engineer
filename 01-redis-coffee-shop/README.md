# Redis Coffee Shop Loyalty System

A hands-on lab demonstrating Redis fundamentals through building a customer loyalty system.

## What You'll Learn

- Redis key-value operations
- Automatic counter management with INCR
- Time-to-live (TTL) for temporary data
- Customer data management patterns

## Prerequisites

- Docker and Docker Compose
- Python 3.8+
- Jupyter Notebook
- `redis` Python package

## Setup

1. **Start Redis:**
   ```bash
   docker-compose up -d
   ```

2. **Install Python dependencies:**
   ```bash
   pip install redis jupyter
   ```

3. **Open the notebook:**
   ```bash
   jupyter notebook coffee_loyalty_system.ipynb
   ```

## Lab Contents

The notebook covers:

1. **Redis Connection** - Connect to local Redis instance
2. **Customer Storage** - Store and retrieve customer information
3. **Visit Tracking** - Implement visit counters with automatic increment
4. **Discount Codes** - Create temporary codes with expiration
5. **Helper Functions** - Build reusable customer management functions
6. **Complete Demo** - End-to-end loyalty system workflow

## Key Redis Concepts

- **SET/GET**: Basic key-value operations
- **INCR**: Atomic counter increment
- **TTL**: Time-to-live for automatic expiration
- **EXISTS**: Check if keys exist
- **Key patterns**: Organized naming conventions (`customer:id`, `visits:id`)

## Cleanup

Stop Redis when done:
```bash
docker-compose down
```