1. Create a catkin workspace
2. Source your setup.bash file or create an alias (http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment)
3. follow the instructions for each package and install them into your workspace 
4. everytime you add a package, make sure to do the follow:
    - cd your_catkin_ws
    - catkin_make

5. everytime you add a new file, make sure to make it executable by:
    - cd location-of-the-file
    - chmod +x name-of-file
6. place the laser_turtlebot.launch file in the turtlebot_bringup folder



### the following steps are to do the gmapping with the gmapping launch file that is provided in the launch files folder:
1. source/ call your alias
2. roscore
3. roslaunch hls_lfcd_lds_driver hlds_laser.launch
4. roslaunch turtlebot_bringup minimal.launch
5. roslaunch turtlebot_bringup laser_turtlebot.launch 
6. roslaunch turtlebot_teleop keyboard_teleop.launch 
7. rviz 
    - in rviz click add to add the map by topic 
    - add turtlebot by clicking tf
8. (if you want to create a rosbag) rosbag record -a


### to save the map http://wiki.ros.org/map_server
1. cd maps
2. rosrun map_server map_saver -f name-the-map
