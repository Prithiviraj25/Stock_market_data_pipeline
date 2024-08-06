# STOCK MARKET DATAPIPLINE USING AWS 

This is a end-to-end data engineering project on stock market data.

## Architecture 

<img src="Architecture.jpg">

## Tech-Stack
- Programming Language - Python
- Amazon Web Service (AWS)
1. S3 (Simple Storage Service)
2. Athena
3. Glue Crawler
4. Glue Catalog
5. EC2
- Apache Kafka

## Methodology

Here for the data i have used a csv file.
now from this csv file using kafka i am using a producer program to produce the data in the json format and the consumer program will dump this data in __AWS S3 BUCKET__

<img src="s3_image.png">

now this data in the S3 bucket will used by the __AWS CRAWLER__ which automatically identifies and catalogs data 

<img src="crawler_image.png">

now this data can be used in the  __AWS ATHENA__ to query and perform simple analytics.

<img src="Athena_image.png">

This is the simple pipeline where real time data can be used to be stored in a data base and be used for querying.

The complete computation is done on __AWS EC2__.

reffer to video below to see how the producer and consumer works and data flows.
[https://github.com/Prithiviraj25/Stock_market_data_pipeline/blob/main/producer_consumer.mov]
and 

["https://github.com/Prithiviraj25/Stock_market_data_pipeline/blob/main/consumer_datapasing.mov"]


# Dataset

The dataset is a csv file [https://github.com/Prithiviraj25/Stock_market_data_pipeline/blob/main/data/indexProcessed.csv] but we can also use web API for real time data 

# Scripts

PRODUCER: [https://github.com/Prithiviraj25/Stock_market_data_pipeline/blob/main/KAFKA_PRODUCER.ipynb]
CONSUMER: [https://github.com/Prithiviraj25/Stock_market_data_pipeline/blob/main/KAFKA_CONSUMER.ipynb]
