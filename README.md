# kafka-RND

1. High trrougput
2. Fault tolarance - replecation tecnique to copy to multiple node.
3. Durable 
4. Sclaable as it is distributed system
5.

zookeeper helps kafka to manage state
Kafka cluster has multiple topics
topics hold different types of messages

download from : https://kafka.apache.org/quickstart
click below : We suggest the following location for your download:



Now upon download -> extract the file

In the command line write :
Initiate zookeeper:  bin\windows\zookeeper-server-start.bat config\zookeeper.properties to execute the kafka
after zooker initiate kafka : bin\windows\kafka-server-start.bat config\server.properties  

kafka will start at 9092



Using docker image
Get the docker image

$ docker pull apache/kafka:3.7.0
Start the kafka docker container

$ docker run -p 9092:9092 apache/kafka:3.7.0



Now kafka server is up and running. Then we have to create topics


Create topic command :
bin\windows\kafka-topics.bat --create --topic topic-name --bootstrap-server localhost:9092

Put messages :
bin\windows\kafka-console-producer.bat --topic user-topic --bootstrap-server localhost:9092

consume message :

bin\windows\kafka-console-consumer.bat --topic user-topic --from-beginning --bootstrap-server localhost:9092
