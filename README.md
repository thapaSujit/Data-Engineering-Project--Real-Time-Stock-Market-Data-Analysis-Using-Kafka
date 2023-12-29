# Stock Market Kafka Real-Time Data Engineering Project

## Introduction
In this project, you will implement an end-to-end Data Engineering solution for processing real-time Stock Market data using Apache Kafka. The project leverages various technologies, including Python, Amazon Web Services (AWS), Apache Kafka, Glue, Athena, and SQL.

## Project Overview
This project is associated with a YouTube video that provides a detailed walkthrough of Docker in general. You can watch the video [here](https://www.youtube.com/watch?v=KerNf0NANMo). The coding for this project was carried out while following the instructions provided in the video.

## Architecture
![Project Architecture](Architecture.jpg)

## Technology Used
- **Programming Language:** Python
- **Amazon Web Services (AWS):**
  1. **S3 (Simple Storage Service):** Used for storing and managing large volumes of streaming data.
  2. **Athena:** Enables querying data directly from S3 using SQL.
  3. **Glue Crawler:** Automatically discovers and catalogs metadata from raw data stored in S3.
  4. **Glue Catalog:** Serves as a centralized metadata repository for Glue and Athena.
  5. **EC2 (Elastic Compute Cloud):** Provides scalable compute capacity for running Python scripts and other processing tasks.

- **Apache Kafka:**
  - **Producer Code (Data Generator):**
    - Utilizes the `kafka-python` library to produce simulated stock market data.
    - Sends data to the 'StockData' Kafka topic.
    - Supports continuous streaming of data to Kafka.

  - **Consumer Code (Data Processor):**
    - Utilizes the `kafka-python` library to consume stock market data from the 'StockData' Kafka topic.
    - Deserializes the data and writes it to individual JSON files on Amazon S3.
    - Demonstrates real-time data processing capabilities.

## Getting Started
1. **Install Dependencies:**
   - infor are provided in command-kafka.txt file

2. **Configure Kafka:**
   - Replace the placeholder IP address (`:9092`) in the producer and consumer code with the actual IP address and port of your Kafka broker.

3. **Run the Producer:**
   - Execute the producer script to simulate and send stock market data to the 'StockData' Kafka topic.

4. **Run the Consumer:**
   - Execute the consumer script to consume real-time data from Kafka and write it to Amazon S3.

## Notes
- The project treats stock data as streaming data, showcasing real-time data processing capabilities.
- Adjust the Kafka broker IP address, port, and S3 bucket details based on your environment.
- This project is a starting point and can be extended to include additional data processing, analysis, and visualization components.

Feel free to explore and enhance the project according to your specific requirements.
