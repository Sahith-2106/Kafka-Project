# Kafka-Project
This architecture demonstrates a real-time data streaming pipeline built using Apache Kafka and AWS services. A Python-based stock market simulation reads data from a dataset and acts as a Kafka producer, publishing events to a Kafka cluster hosted on Amazon EC2. 

Kafka serves as the central messaging layer, decoupling data producers from consumers and enabling scalable, fault-tolerant streaming. A Kafka consumer processes the incoming events and stores the data in Amazon S3 as the data lake.

An AWS Glue Crawler scans the stored data in S3 and updates the Glue Data Catalog, making the data discoverable and query-ready. Finally, Amazon Athena is used to run SQL queries directly on the data in S3 for analytics and insights, without requiring data movement.


## Architecture Flow
1. Stock market data is read from a CSV dataset.
2. A Python application publishes data to Apache Kafka as a producer.
3. Apache Kafka runs on an Amazon EC2 instance.
4. Kafka consumers process the data and write it to Amazon S3.
5. AWS Glue Crawler scans S3 data and updates the Glue Data Catalog.
6. Amazon Athena queries the data using SQL.


## Technologies Used
- Python  
- Apache Kafka  
- Amazon EC2  
- Amazon S3  
- AWS Glue  
- Amazon Athena  


# Project Structure

├── data/
│   └── Data.csv
├── producer/
│   └── kafka_producer.ipynb
├── consumer/
│   └── kafka_consumer.ipynb
├── scripts/
│   └── command_kakfka.txt
├── architecture/
│   └── architecture-Kafka.png
└── README.md
