## Simulation Setup

### Fetch Install Guide:
    - Clone the repo in `catkin_ws/src` folder and cd into catkin_ws.
    - Source ros noetic install.
    - `rosdep update`
    - In folder 'WHR_simulation/simple_grasping', clone from the following directory: 'https://github.com/mikeferguson/simple_grasping.git'
        - `cd WHR_simulation/simple_grasping`
        - `git clone https://github.com/mikeferguson/simple_grasping.git`
    - `rosdep install --from-paths src/ --ignore-src --rosdistro noetic`
    - `catkin_make`

### Fetch Run Guide:
    - Source ros noetic if you haven’t already (do this before running any ros command):
        source /opt/ros/noetic/setup.bash
    - Source development setup: 
        cd ~/catkin_ws && source devel/setup.bash
    - Run robot by in empty environment: `roslaunch fetch_gazebo simulation.launch robot:=freight`
    - Run Robot in Warehouse: 
        roslaunch fetch_gazebo simple_warehouse.launch robot:=freight
    - Run robot in playground environment
        roslaunch fetch_gazebo playground.launch robot:=freight
    - On a separate terminal, run teleoperation: 
        rosrun teleop_twist_keyboard teleop_twist_keyboard.py

### Rviz Visualization Guide:
    - Run `rosrun rviz rviz` after you have finnished all the above steps
    - In rviz window, select `base_camera_optical_frame` as the frame.
    - Add camera topic: `/camera/Color/Image_Raw/Camera`
    - Add pointcloud topic: `/camera/depth/points/Pointcloud`