## Kafka CLI

- To start Zookeeper:
 zookeeper-server-start.sh config/zookeeper.properties

- To start Server Apache Kafka:
 kafka-server-start.sh config/server.properties

- To list the topics of broker:
kafka-topics.sh --zookeeper 127.0.0.1:2181 --list

- To create a new topic:
kafka-console-producer.sh --broker-list 127.0.0.1:9092
--topic new_topic

- To consume the topic:
kafka-console-consumer.sh --bootstrap-server 127.0.0.1:9092 --topic first_topic

- To create a producer:
kafka-console.producer.sh --broker-list 127.0.0.1:9092 --topic first_topic
