# smart-grids-sgbi
Smart Grids: Infraestructura, gestión del dato y BI (SGBI)

## Quick Start

### Start the services
```bash
docker-compose up -d
```

## Kafka
### Access to Kafka container
```bash
docker exec -it kafka bash
```

### Execute the scripts to test Kafka
```bash
kafka-topics.sh --create --topic test --bootstrap-server localhost:9092 --partitions 3 --replication-factor 1
```

```bash
kafka-console-producer.sh --topic test --bootstrap-server localhost:9092
```

## Spark
### Start the Spark container
```bash
docker start spark
```

### Execute the scripts to test Spark Streaming
```bash
spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.12:3.5.1 /opt/spark-apps/spark_consumer.py
```

## TimescaleDB
### Check the data in TimescaleDB
```bash
docker exec -it timescaledb psql -U myuser -d mydb
```
