# Flink-eCommerce

This repository contains an Apache Flink application for real-time sales analytics built using Docker Compose to orchestrate the necessary infrastructure components, including Apache Flink, Elasticsearch, and Postgres. The application processes financial transaction data from Kafka, performs aggregations, and stores the results in both Postgres and Elasticsearch for further analysis.


System Architecture:
![System Architecture](https://github.com/darshan601/Flink-eCommerce/blob/main/System%20Architecture.png?raw=true)


## Requirements
- Docker
- Docker Compose

## Installation and Setup
1. Clone this repository.
2. Navigate to the repository directory.
3. Run `docker-compose up` to start the required services.
4. Use `main.py` from the Sales Transaction Generator to generate sales transactions into Kafka.

## Usage
1. Ensure all Docker containers are up and running.
2. Run the `FlinkCommerce` application for real-time analytics on financial transactions.

## Components
- **Apache Flink**: Processes and transforms transaction data from Kafka.
- **Postgres**: Stores transaction data and aggregated results.
- **Elasticsearch**: Indexes transaction data for further analysis.

## Code Structure
- `DataStreamJob.java`: Main Flink application logic.
- `Deserializer`, `Dto`, `utils` packages: Classes and utilities for data handling.

## Configuration
- Kafka settings: Configured within the Kafka source setup.
- Postgres connection: Defined in the `jdbcUrl`, `username`, and `password` variables.


reference:
https://github.com/airscholar/FlinkCommerce
