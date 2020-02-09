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
```

### Start a consumer with group:

```
kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic first-topic --group first-application
```

```
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
## Reset offset:

Reset the consumer offset for a topic for preview: This will print the expected result of the reset, but not actually run it.

```
kafka-consumer-groups.sh --bootstrap-server localhost:9092 --group first-application --topic first-topic --reset-offsets --to-earliest --dry-run
```

Reset the consumer offset for a topic (execute):

```
kafka-consumer-groups.sh --bootstrap-server localhost:9092 --group first-application --topic first-topic --reset-offsets --to-earliest --execute
```

Error: Assignments can only be reset if the group 'first-application' is inactive, but the current state is Stable.

How to fix: We have to stop all comsumers in the group.

# 🌟CLI Options that are good to know:



The CLI have many options, but here are the other that are most commonly used:

Producer with keys:
```
kafka-console-producer.sh --broker-list 127.0.0.1:9092 --topic first-topic --property parse.key=true --property key.separator=,
> key,value
> another key,another value
```

Consumer with keys:
```
kafka-console-consumer.sh --bootstrap-server 127.0.0.1:9092 --topic first-topic --from-beginning --property print.key=true --property key.separator=,
```

