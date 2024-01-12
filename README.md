 To run the demo

# Start the broker

```
docker run -it --rm -p 8161:8161 -p 61616:61616 -p 5672:5672 -e AMQ_USER=foo -e AMQ_PASSWORD=bar quay.io/artemiscloud/activemq-artemis-broker:1.0.21
```

# Run the consumer app

```
cd consumer;
./gradlew run
```

# Run the producer app

```
cd producer;
./gradlew run
```

You will see in the consumer logs: 

```
10:34:05.666 [Thread-0 (ActiveMQ-client-global-threads)] INFO  consumer.PriceConsumer - received 24
```
