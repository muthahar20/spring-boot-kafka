# spring-boot-kafka

Spring boot kafka application with multiple Producers and multiple Consumers for String data and JSON object - This project explains How to publish message in kafka Topic and consume a message from Kafka Topic. Here message is in String and Json Object format.
In this application there are two publishers, i.e. one for String data and another one is for publishing object. For those two publishers, two KafkaTemplates are used.
To consume those messages and objects two consumers are used. Two KafkaListners are used to consume respective data.

Prerequisites: Java, Sprong Boot, Kafka and Zookeeper

ZooKeeper Framework Installation
Download ZooKeeper
--------------------
download the latest version of ZooKeeper. http://zookeeper.apache.org/releases.html

Extract the tar file using the following commands −
$ cd opt/
$ tar -zxf zookeeper-3.4.6.tar.gz
$ cd zookeeper-3.4.6
$ mkdir data

Create configuration file
Open the configuration file named conf/zoo.cfg using the command vi conf/zoo.cfg and all the following parameters to set as starting point.

$ vi conf/zoo.cfg

tickTime = 2000
dataDir = /path/to/zookeeper/data
clientPort = 2181
initLimit = 5
syncLimit = 2

:wq  --> save file on Vi Editor

Once the configuration file has been saved successfully, return to the terminal again. You can now start the zookeeper server.
Start ZooKeeper server:
$ bin/zkServer.sh start

Start CLI
$ bin/zkCli.sh

After typing the above command, you will be connected to the ZooKeeper server and you should get the following response.
Connecting to localhost:2181
................
................
................
Welcome to ZooKeeper!
................
................
WATCHER::
WatchedEvent state:SyncConnected type: None path:null
[zk: localhost:2181(CONNECTED) 0]

Stop ZooKeeper Server:
$ bin/zkServer.sh stop



--------

#Code Snippets:
  #Maven Dependencies:
    #add below dependency to enable kafka in pom.xml
    <dependency>
    <groupId>org.springframework.kafka</groupId>
    <artifactId>spring-kafka</artifactId>
    </dependency>


    #Properties file
    #src/main/resources/application.yml

    spring:
  kafka:
    consumer:
      bootstrap-servers: localhost:9092
      group-id: group_id

    producer:
      bootstrap-servers: localhost:9092

    topic: message-topic
    superhero-topic: superhero-topic  


    





