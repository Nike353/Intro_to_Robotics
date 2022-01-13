# Intro to Jackal-Robot and controlling the robot using ROS and Rviz
## Installation
### Installing git 
```
sudo apt-get install git
```
### Installing Jackal Simulation
```
sudo apt-get install ros-melodic-jackal-simulator ros-melodic-jackal-desktop
```
### Creating a catkin workspace
```
cd ~
mkdir -p jackal_bot/src
cd jackal_bot
```
### Building and sourcing  the workspace
```
catkin build
source ./devel/setup.bash
```
### Installing the packages
```
cd jackal_bot/src
git clone https://github.com/jackal/jackal.git
git clone https://github.com/jackal/jackal_simulator.git
git clone https://github.com/clearpathrobotics/LMS1xx.git
git clone https://github.com/ros-drivers/pointgrey_camera_driver.git
cd ..
```
### Building  and sourcing again 
```
catkin build
source devel/setup.bash
```

### Launching jackal in gazebo
#### To launch simulated Jackal in a simple example world, run the following command:
```
roslaunch jackal_gazebo jackal_world.launch
```
#### To launch the Jackal along configured laser or camera
```
roslaunch jackal_gazebo jackal_world.launch config:=front_laser
roslaunch jackal_gazebo jackal_world.launch config:=front_bumblebee2
roslaunch jackal_gazebo jackal_world.launch config:=front_flea3
```

### Launching Jackal in Rviz 
```
roslaunch jackal_viz view_robot.launch
```

## Creating a custom package to control the jackal robot
```
cd ~/jackal_robot/src
catkin_create_pkg tele_op std_msgs rospy roscpp
cd ..
catkin build
```




