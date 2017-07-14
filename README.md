# kafka-twitter-webScraping

Kafka Twitter source connector combined with Kafka Hdfs/Hive sink connector to read live Twitter feed, serialize the intermediate message in Avro format and finally output each tweet to Hdfs in Parquet format.
This data can also be queried using Hive external table schema.

Custom Scrapy crawler, can parse each review using an Avro schema and store them in Hdfs using Avro format. Again, this data can be queried using Hive. Crawler is written in Python and primarily uses xpath along with advanced features like user-agent spoofing and IP rotation. It uses a native Kafka client (as Kafka producer) which is also supplied by Confluent.

