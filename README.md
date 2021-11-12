# kafkaserver

Kakfa Server installation using Docker
Prerequisites:
   - Install docker-compose

docker-compose -f docker-compose.yaml up -d

docker images

docker ps

docker exec -it kafka /bin/bash
#inside container
  cd opt/bitnami/kafka/bin
  ls
  # create kafka topics
  kafka-topics.sh --create --zookeeper zookeeper:2181 --replicaton-factor 1 --partitions 1 --topic mytopic1
  kafka-topics.sh --create --zookeeper zookeeper:2181 --replicaton-factor 1 --partitions 1 --topic mytopic2
  # list the topics
  kafka-topics.sh --list --zookeeper zookeeper:2181

