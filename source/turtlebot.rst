Turtlebot
=========

The turtlebot is a groud robots with a kinect cemera. The robot can move around and it can see both depth images and color images through the Kinect camera.

Objective
---------

The objective of this project is to control the Turtlebot by processing the data coming from the Kinect camera.

Deploy on Storm
---------------

1. Build the processor module i.e. 
   mvn clean install 
2. Go to the storm directory
   cd ~/storm_home
3. Run the storm command

./bin/storm jar path_to_jar_file cgl.iotrobots.st.storm.SphereTrackingTopology st
 
 Here is an example
 
./bin/storm jar ~/projects/iotrobots/drone/processor/target/drone-processor-1.0-SNAPSHOT-jar-with-dependencies.jar cgl.iotrobots.st.storm.DroneProcessorTopology -url amqp://10.39.1.16:5672 -name drone_processor -ds_mode 2

Deploy the sensor
-----------------

1. Build the sensor module and copy the jar with dependencies to repository/sensors directory of IOTCloud
2. Go to IOTCloud master and Run the command

./bin/iotcloud jar repository/sensors/drone-sensor-1.0-SNAPSHOT-jar-with-dependencies.jar cgl.iotrobots.st.STSensor -url amqp://10.39.1.16:5672

-url argument gives the URL of the local RabbitMQ server, where the Drone sends video messages
