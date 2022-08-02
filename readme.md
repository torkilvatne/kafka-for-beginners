# Introduction to Kafka from Udemy

## Helpful commands
For helpful commands, see the 'help'-folder.

## Setup Wikimedia example

Start zookeeper and kafka in different terminals:
```
$ zookeeper-server-start.sh ~/Documents/kafka_2.13-3.2.0/config/zookeeper.properties
$ kafka-server-start.sh ~/Documents/kafka_2.13-3.2.0/config/server.properties
```

Create a kafka topic:
```
$ kafka-topics.sh --bootstrap-server 127.0.0.1:9092 --create --topic wikimedia.recentchanges --partitions 3 --replication-factor 1
```

Start a kafka consumer:
```
$ kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic wikimedia.recentchanges --from-beginning
```

Then start WikimediaChangesProducer.


