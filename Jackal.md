# Intro to Jackal-Robot and controlling the robot using ROS and Rviz
## Installation
#### Installing git 
```
sudo apt-get install git
```
#### Installing Jackal Simulation
```
sudo apt-get install ros-kinetic-jackal-simulator ros-kinetic-jackal-desktop
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
### Building again 
```
catkin build
```




