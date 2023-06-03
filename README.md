# kafka-cluster-ssl

This repo has the repo for the kafka-cluster-ssl.

## Generate the required certs for setting up the ssl secured cluster

- Navigate to the **secrets** directory.

- Run the below command.

```script
sh create-certs.sh
```

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


```agsl
docker exec --interactive --tty kafka1  \
kafka-console-consumer --bootstrap-server localhost:9092 \
                       --topic library-events \
                       --from-beginning \
                       --consumer.config /etc/kafka/properties/consumer.properties

```
