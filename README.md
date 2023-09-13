# spring-boot-kafka

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



