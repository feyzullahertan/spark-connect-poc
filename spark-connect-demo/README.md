# Spark Connect Demo

This project demonstrates how to use Apache Spark 4.0 with Spark Connect via Docker.

## Requirements
- Write idiomatic spark code
- Little docker knowledge

## Getting Started

```bash
git clone <this-repo>
cd spark-connect-demo
docker-compose up --build
```

Access Jupyter Notebook at: [http://localhost:8888](http://localhost:8888)

## 🔗 Spark Connect Info
This repo uses `pyspark-connect` to connect to a remote Spark server via gRPC.

Example:

```python
from pyspark.sql import SparkSession
spark = SparkSession.builder.remote("sc://spark-connect:15002").getOrCreate()
```

## Folder Structure
- `spark/`: Spark Connect server (based on Spark 4.0)
- `notebook/`: Contains example notebook
- `data/`: Sample CSV data

