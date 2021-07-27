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
To assigned a group:
--group <Group> 
To get from begining:
--from-begining
To list consumer group:
kafka-consumer-groups.sh --bootstrap-server localhost:9092 --list my-first-app
Get info about consumer groups:
kafka-consumer-groups.sh --bootstrap-server localhost:9092 --describe --group my-first-app
To Reset offsets of consumer:
kafka-consumer-groups.sh --bootstrap-server localhost:9002 --group my-first-app --reset-offsets --to-earliest --execute --topic first_topic
