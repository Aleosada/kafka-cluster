# Create credentials
```
kafka-configs --zookeeper zookeeper-1:2181 --alter --add-config 'SCRAM-SHA-256=[iterations=8192,password=broker-secret]' --entity-type users --entity-name broker
kafka-configs --zookeeper zookeeper-1:2181 --alter --add-config 'SCRAM-SHA-256=[iterations=8192,password=producer-secret]' --entity-type users --entity-name producer
kafka-configs --zookeeper zookeeper-1:2181 --alter --add-config 'SCRAM-SHA-256=[iterations=8192,password=consumer-secret]' --entity-type users --entity-name consumer
```
