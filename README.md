# Covid-19-Data-Pipeline-Based-On-Messaging-and-Analysis
## Building data pipeline for Covid-19 data analysis using BigData technologies and Tableau

* The purpose is to collect the real time streaming data from COVID19 open API for every 5
minutes into the ecosystem using NiFi and to process it and store it in the data lake on
AWS.Data processing includes parsing the data from complex JSON format to csv format then
publishing to Kafka for persistent delivery of messages into PySpark for further processing.The
processed data is then fed into output Kafka topic which is inturn consumed by Nifi and stored in
HDFS .A Hive external table is created on top of HDFS processed data for which the process is
Orchestrated using Airflow to run for every time interval. Finally KPIs are visualised in tableau.

![Alt text](Architecture.png?raw=true "Title")

* Tools used
-------------------------------
1. Nifi -nifi-1.10.0
2. Hadoop -hadoop_2.7.3
3. Hive-apache-hive-2.1.0
4. Spark-spark-2.4.5
5. Zookeeper-zookeeper-2.3.5
6. Kafka-kafka_2.11-2.4.0
7. Airflow-airflow-1.8.1
8. Tableau

* Visualization using Tableau
---------------------------------------
![Alt text](visualization.jpg?raw=true "Title")
