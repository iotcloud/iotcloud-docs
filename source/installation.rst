Installation
============

First we need to build the projects. Please refer the source page for more information.

To deploy a sensor and process its data you need to run

1. Apache ZooKeeper
2. IOTCloud
3. RabbitMQ Server
4. Apache Storm

Please refer Apache ZooKeeper installtion guide, RabbitMQ server installtion guide and Apache Storm installtion guide for how to deploy and run them.

We will focus on running IOTCloud here. First we need to build the IOTCloud project as described in the source section.

The various configurations for the IOTCloud can be found in the conf/iot.yaml file.

Standalone Mode
---------------

You need to Run Apache ZooKeeper first to run IOTCloud.

Extract the IOTCloud and go to the iotcloud folder. The run

./bin/iotcloud local

This will start a master and site server on the same JVM.

Distributed Mode
----------------

To run in distributed mode, we need to first run a Master node.

./bin/iotcloud master


Then we need to run a site node by typing

./bin/iotcloud site


Make sure the site nodes master IP configuration is pointing to the master node.


