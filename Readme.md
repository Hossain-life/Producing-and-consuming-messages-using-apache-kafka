First I downloaded the latest version of JDK by visiting the following link http://www.oracle.com/technetwork/java/javase/downloads/index.html. Files downloaded 
are stored in the downloads folder, and then, I verified it and extracted the tar setup using the following commands($ cd /go/to/download/path
$ tar -zxf jdk-8u60-linux-x64.gz). Subsequently, I edited the environment variables in control panel where I set my java_home path and kafka path. I also configured the
zookeeeper properties and server properties. After that, I started the zookeeper server on windows using a command(.\bin\windows\zookeeper-server-start.bat), and then, I started
running a kafka server using the following command(.\bin\windows\kafka-server-start.bat .\config\server.properties). As my aim was to produce and consume messages in apache kafka, I 
created two topics in the zookeeper which are Testtopic and newtopic. In the testtopic, I entered some messages in the producer console using the following command(.\bin
\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic Testtopic). To see the output, I printed the messages in the consumer console using the following command(.\bin
\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic Testtopic --from-beginning).
