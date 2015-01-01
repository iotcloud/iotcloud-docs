Source Code
===========

There are four main projects related to IOTCloud project. Those projects can be found in

1. The gateways connecting sensors to applications : https://github.com/iotcloud/iotcloud2.git
2. The pub-sub connector library from sensors to cloud services: https://github.com/iotcloud/storm-broker-connectors.git
3. The discovery service library for sensor applications: https://github.com/iotcloud/sensorstream.git
4. The robotic applications: https://github.com/iotcloud/iotrobots.git

Requirements
------------

To build and run IoTCloud and its application you need JDK 1.6 or above and Python 2.7 or above.
The projects use the maven build system. So if you are trying to build the source you need Maven 3.

1. JDK 1.6 or above
2. Python 2.7
3. Apache Maven

The build steps are explained in the order a new user should build the system.

storm-broker-connectos
----------------------

These are libraries developed to connect the sensor data to Storm using pub-sub messaging. At the moment we
have developed libraries for RabbitMQ, Kafka, Kestrel and JMS. We primarily use RabbitMQ as our pub-sub broker.

First download the source to your machine.

git clone https://github.com/iotcloud/storm-broker-connectors.git

Go to the storm-broker-connectors folder and type

mvn clean install

This will build the project. The built libraries (jar files) will be added to the maven local repository
and these will be used by the other projects automatically.


IOTCloud 
--------

This is the project that has the Gateways. The sensor applications are developed using this project and deployed in IoTCloud server.
IoTCloud has two servers and they are the master and site servers. The sensors are deployed in the site servers.

git clone https://github.com/iotcloud/iotcloud2.git

To compile IOTCloud project, go to the iotcloud folder and type

mvn clean install

This will compile the project. IoTCloud has two servers that you need to run.
IoTCloud is built as a software distribution. This distribution is not build in the previous step.

To build the distribution go to the iotcloud/distribution folder and type

mvn clean install

This will build the distribution as a tar and zip archive in the target folder of distributio folder.
This archive can be extracted to run the iotcloud project.

sensorstream
------------

This is a library that is used by IoTCloud and Storm to dynamically discover the sensors.

git clone https://github.com/iotcloud/sensorstream.git

Go to the sensorstream folder and type

mvn clean install

This will build the project.

iotrobots
---------

This project includes the sensor applications we are developing using the above platform. The sensor applications include

1. Autonomous drone control
2. TurtleBot follower
3. SLAM
4. Collision Avoidance
5. Performance measuring applications

git clone https://github.com/iotcloud/iotrobots.git

Go to the iotrobots folder and type

mvn clean install

This will build the project.


