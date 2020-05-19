# kafka-basic-commands
To download the file go to the [link](https://www.apache.org/dyn/closer.cgi?path=/kafka/2.5.0/kafka_2.12-2.5.0.tgz) and save the file in c:\ folder. Now open the powershell as an administrator and execute the commands ```tar -xzf kafka_2.12-2.5.0.tgz```,  this will <b>un-zip the folder</b> and now you can see the extracted <b>kafka_2.12-2.5.0</b> file and use ```cd kafka_2.12-2.5.0``` to enter into the folder if required.
- To<b> start the zookeeper server</b>, in a new powershell window, enter the command ```.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties``` 
- To <b>start the kafka server</b>, in a new powershell window, enter the command ```.\bin\windows\kafka-server-start.bat .\config\server.properties```
- To <b>create a topic</b> in this, open a new powershell and enter the command ```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic {topic_name}```
- To view the <b>list of topics</b> present, enter the command ```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list```
- Now to enter the <b>topic as a producer</b>, in a new powershell window enter the command ```.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic {topic_name}```. Then you can enter any message you want to send and that meaasage will be delivered dynamically to other customer tabs.
- To view the <b>topic as a customer</b>, in a new powershell enter the command ```.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic {topic_name} --from-beginning```

# My custom commands
I have selected topic as <b>weatherReport</b>. So according to the steps above 
- To start zookeeper server, the command is ```.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties``` 
- To start kafka server, the command is ```.\bin\windows\kafka-server-start.bat .\config\server.properties```
- To create a topic the command is ```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --create --topic weatherReport```
- To view the list of topics, the command is ```.\bin\windows\kafka-topics.bat --zookeeper localhost:2181 --list```. We can be able to see the name <b>weatherReport</b> in the list displayed.
- To be a producer of the topic weatherReport, the command is ```.\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic weatherReport```. Now we will be able to enter message to the topic
- To be a customer of the topic weatherReport, the command is ```.\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic weatherReport --from-beginning```. Now the messages sent by the producer from beginning are displayed below.
