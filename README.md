# Kafka

Question: What is Apache Kafka and what are its main use cases?
Answer: Apache Kafka is a open source distributed streaming system used for stream processing, real time data pipeline and data integration at scale.

Use Cases:
  1. Log Agrregation
  2. Real time streaming
  3. data streaming
  4. microservice communication
  5. ETL pipelines

**Question**: Explain the key components of kafka.
**Answer**: Kakfka works on event driven architecture where producer (client app/connector) will send messages to broker (kafka server) which will be consumed by consumer (client app/connector).

**Producer**: App/Connector which sends messages/event logs to broker. it generates unique id for each message and serilizes messages and pass to network buffer which will be sent to brocker. Producre can be scaled and its producers responsibility to generate unique id for which producer will have unique sequence id generated by broker and assigned during bootstrapping.
**Broker**: Broker is a single kafka server which receives messages from producer and generates offset for each message and stores messages into disk storage.
**Consumer**: Consumer is an app/connector which will consume messages from broker and each consumer is assigned to a consumer group. means multiple consumer can read messages simultanously from same topic for that each consumer will be allowed to read messages from a single partition. 

**Topic**: Topic is a categorization event logs which will group same type of messages.
**Partitions**: Partition meanes distributing workloads evenly to multiple brokers. kafka will partition a topic and will keep partions on multiple servers this way system will be scalable and also will replicate partions for fault tolerance.

     
