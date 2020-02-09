# 🌟Zookeeper:

```
zookeeper-server-start.sh config/zookeeper.properties
```
# 🌟 Kafka server:
```
kafka-server-start.sh config/server.properties
```

# 🌟Topic:

```
kafka-topics.sh --create --bootstrap-server localhost:9092 --partitions 3 --topic first-topic

kafka-topics.sh --create --bootstrap-server localhost:9092 --partitions 3 --replication-factor 3 --topic first-topic

kafka-topics.sh --list --bootstrap-server localhost:9092


```

# 🌟Producer:

```
kafka-console-producer.sh --broker-list 127.0.0.1:9092 --topic first-topic
```

# 🌟Consumer:

```
kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic first-topic

kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic first-topic --from-beginning

kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic first-topic --group first-application

# --from-beginning is only affect for the first time creating a group
kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic first-topic --group third-application --from-beginning

```

# 🌟 Consumer Group:
### List all consumer groups: 

```
kafka-consumer-groups.sh --bootstrap-server localhost:9092 --list
```

### Describe consumer group and list offset lag (number of messages not yet processed) related to given group:
```
kafka-consumer-groups.sh --bootstrap-server localhost:9092 --describe --group first-application
```
