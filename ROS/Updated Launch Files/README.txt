turtlebot2 (call alias)
roslaunch hls_lfcd_lds_driver hlds_laser.launch (launch the lidar scanner)
roslaunch hector_slam_launch tutorial.launch (open hector slam launch file)



cd /maps/
rosrun map_server map_saver -f <name> (to save the map)




rostopic pub syscommand std_msgs/String "savegeotiff"

cd <where your rosbag folder is>
rosbag record <name of file without .bag>
ctrl+c to stop recording






TO USE GMAPPING IN AN ENVIRONMENT LOADED INTO GAZEBO 

turtlebot2
roslaunch turtlebot_gazebo turtlebot_world.launch
(launches turtlebot inside of a world)

roslaunch turtlebot_gazebo gmapping_demo.launch
(can gmap in the created world)

rviz
(to visualize the gmapping)

roslaunch turtlebot_teleop keyboard_teleop.launch
(manually navigate to create the map inside of the digital world)

