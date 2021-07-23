# template
Comandos básicos para utilização do projeto no Kafka

- Sobe o Zookeeper
.\zookeeper-server-start.bat ..\..\config\zookeeper.properties

- Sobe o Kafka
.\kafka-server-start.bat ..\..\config\server.properties

- Descreve os tópicos criados no kafka
.\kafka-topics.bat --describe --bootstrap-server localhost:9092

- Consumindo tópico desde offset 0
.\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic ECOMMERCE_NEW_ORDER --from-beginning

- Alterando um tópico para ter 3 partições:
.\kafka-topics.bat --alter --zookeper localhost:2181 --topic ECOMMERCE_NEW_ORDER --partitions 3
