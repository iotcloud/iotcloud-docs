Source Code
===========

There are three projects in IOTCloud project. Those projects can be found in

1. The gateways connecting sensors to applications : https://github.com/iotcloud/iotcloud2.git
2. The pub-sub connectors from sensors to cloud services: https://github.com/iotcloud/storm-broker-connectors.git
3. The discovery services for sensor applications: https://github.com/iotcloud/sensorstream.git
4. Tje actual robotics code: https://github.com/iotcloud/iotrobots.git

All these projects require JDK 1.6 or above and Python 2.7 or above. The projects mainly use the maven build system for compilation. 

1. JDK 1.6 or above
2. Python 2.7
3. Maven 

git is required to get a clone of the project as well.

The build steps are explained in the order a new user should build the system

storm-broker-connectos
----------------------

Go to the storm-broker-connectors folder and type

mvn clean install

This will build the project.


IOTCloud 
--------

To compile IOTCloud project, go to the iotcloud folder and type

mvn clean install

This will compile the project. To build the distribution go to the iotcloud/distribution folder and type 

mvn clean install

This will build the distribution as a tar and zip archive in the target folder of distributio folder. This archive can be extracted to run the iotcloud project.

sensorstream
------------

Go to the sensorstream folder and type

mvn clean install

This will build the project.

iotrobots
---------

Go to the iotrobots folder and type

mvn clean install

This will build the project.
