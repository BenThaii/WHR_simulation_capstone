# Freight Robot in based on Turtlebot3 Sim

# Installation
* Clone This repo
* Install dwa-planner using `sudo apt install ros-noetic-dwa-local-planner`
* Run catkin_make
* Make sure latest version of rtabmap is in your workspace

# Start Navigation and Mapping

Run following commands in one terminal after sourcing your catkin worspace: 
* `roslaunch freight_gazebo freight_world.launch`

For teleoperation, run:
* `roslaunch freight_teleop freight_capstone_teleop_key.launch`