# kafka-cluster-ssl

This repo has the repo for the kafka-cluster-ssl.

## Produce/Consumer Messages in a SSL Secured Environment

- Produce Messages to the topic.

```
docker exec --interactive --tty kafka1  \
kafka-console-producer --bootstrap-server localhost:9092 \
                       --topic test-topic \
                       --producer.config /etc/kafka/properties/producer.properties
                       
```

- Produce Messages to the topic.

```
docker exec --interactive --tty kafka1  \
kafka-console-consumer --bootstrap-server localhost:9092 \
                       --topic test-topic \
                       --from-beginning \
                       --consumer.config /etc/kafka/properties/consumer.properties
```