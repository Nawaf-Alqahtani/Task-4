# Task-4  Using SLAM map to launch the navigation

# In this task I ran and wrote commands to start navigating the SLAM map using the Rviz and Gazebo emulator.


1.Launch Simulation World:

$ export TURTLEBOT3_MODEL=burger

$ roslaunch turtlebot3_gazebo turtlebot3_world.launch

2.Run Navigation Node:

$ export TURTLEBOT3_MODEL=burger

$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml




3.Estimate Initial Pose:

1. I Click the 2D Pose Estimate button in the RViz menu.

2. I click on the map where the actual robot is located and drag the large green arrow toward the direction where the robot is facing.


3. I repeat step 1 and 2 until the LDS sensor data is overlayed on the saved map.


4. I Launch keyboard teleoperation node to precisely locate the robot on the map.


$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

5. I move the robot back and forth a bit to collect the surrounding environment information and narrow down the estimated location of the TurtleBot3 on the map which is displayed with tiny green arrows.

![nav pose](https://user-images.githubusercontent.com/85695324/125962323-351b726c-4afd-41e1-9afb-0d7b981f532c.png)

6. I terminate the keyboard teleoperation node by entering Ctrl + C to the teleop node terminal in order to prevent different cmd_vel values are published from multiple nodes during Navigation.


4.Set Navigation Goal:

1. I click the 2D Nav Goal button in the RViz menu.

2. I click on the map to set the destination of the robot and drag the green arrow toward the direction where the robot will be facing.

![nav goal](https://user-images.githubusercontent.com/85695324/125964442-1b04efbc-daff-4ed9-816c-64de5708b96c.png)


