
Všechny soubory potřeba vložit ke složce models, aby vše fungovalo. 



LIDAR

Příkazy:

terminal A

gz launch robot_lights_ON_3_doors_open_world.gzlaunch

terminal B

ros2 run ros_gz_bridge parameter_bridge /lidar@sensor_msgs/msg/LaserScan[ignition.msgs.LaserScan --ros-args -r /lidar:=/laser_scan

terminal C

source /opt/ros/humble/setup.bash
rviz2




Nastaveni Rviz:

Fixed frame: vehicle_blue/chassis/gpu_lidar

ADD -> by topic -> LaserScan



Kamera

Příkazy:

terminal A

gz launch robot_lights_ON_3_doors_open_world.gzlaunch

terminal B

ros2 run ros_gz_bridge parameter_bridge /camera@sensor_msgs/msg/Image[ignition.msgs.Image --ros-args -r /camera:=/camera_image


terminal C

source /opt/ros/humble/setup.bash
rviz2




Nastaveni Rviz:

Fixed frame: vehicle_blue/chassis/camera

ADD -> by topic -> Image

