# Task-4  Using SLAM map to launch the navigation

# In this task I ran and wrote commands to start navigating the SLAM map using the Rviz and Gazebo emulator.


1.Launch Simulation World:

$ export TURTLEBOT3_MODEL=burger

$ roslaunch turtlebot3_gazebo turtlebot3_world.launch

2.Run Navigation Node:

$ export TURTLEBOT3_MODEL=burger

$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml




3.Estimate Initial Pose:

$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

4.Set Navigation Goal:

