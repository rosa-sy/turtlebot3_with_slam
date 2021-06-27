# turtlebot3_with_slam
---
Use Turtlebot3 with SLAM approach to create and save a map
---
## Install package
---
sudo apt-get install ros-melodic-joy

sudo apt-get install ros-melodic-teleop-twist-joy

sudo apt-get install ros-melodic-teleop-twist-keyboard

sudo apt-get install ros-melodic-laser-proc

sudo apt-get install ros-melodic-rgbd-launch

sudo apt-get install ros-melodic-depthimage-to-laserscan

sudo apt-get install ros-melodic-rosserial-Arduino

sudo apt-get install ros-melodic-rosserial-python

sudo apt-get install ros-melodic-rosserial-server

sudo apt-get install ros-melodic-rosserial-client

sudo apt-get install ros-melodic-rosserial-msgs

sudo apt-get install ros-melodic-amcl

sudo apt-get install ros-melodic-map-server

sudo apt-get install ros-melodic-move-base

sudo apt-get install ros-melodic-urdf

sudo apt-get install ros-melodic-xacro

sudo apt-get install ros-melodic-compressed-image-transport

sudo apt-get install ros-melodic-rqt-image-view

sudo apt-get install ros-melodic-gmapping

sudo apt-get install ros-melodic-navigation

sudo apt-get install ros-melodic-dynamixel-sdk

sudo apt-get install ros-melodic-turtlebot3-msgs

sudo apt-get install ros-melodic-turtlebot3
## Set TurtleBot3 Model Name
---
echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
---
# Install Simulation Package
---
## Gazebo Simulation
---
### 1-Empty World

export TURTLEBOT3_MODEL=burger

roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch

![photo_2021-06-27_15-14-54](https://user-images.githubusercontent.com/85003576/123544192-ce1d7e80-d75a-11eb-9f4a-c17b89995af8.jpg)
---
### 2-Turtlebot3 World

export TURTLEBOT3_MODEL=waffle

roslaunch turtlebot3_gazebo turtlebot3_world.launch

![photo_2021-06-27_15-13-32](https://user-images.githubusercontent.com/85003576/123544212-ebeae380-d75a-11eb-90cb-5e009c76bf0b.jpg)
---
### 3-Turtlebot3 House

export TURTLEBOT3_MODEL=waffle_pi

roslaunch turtlebot3_gazebo turtlebot3_house.launch

![photo_2021-06-27_15-15-06](https://user-images.githubusercontent.com/85003576/123544758-69175800-d75d-11eb-9420-a1d2d984278c.jpg)

---
## SLAM Simulation
---
### 1-Launch Simulation World

export TURTLEBOT3_MODEL=burger

roslaunch turtlebot3_gazebo turtlebot3_world.launch

---
### 2-Run SLAM Node

export TURTLEBOT3_MODEL=burger

roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping

---
### 3-Run Teleoperation Node

export TURTLEBOT3_MODEL=burger

roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch

Control Your TurtleBot3!

![photo_2021-06-27_15-13-11](https://user-images.githubusercontent.com/85003576/123544264-23f22680-d75b-11eb-9d13-41803f919ffa.jpg)

 ---------------------------
 Moving around:
        w
   a    s    d
        x

 w/x : increase/decrease linear velocity
 
 a/d : increase/decrease angular velocity
 space key, s : force stop

 CTRL-C to quit
 
![photo_2021-06-27_15-13-21](https://user-images.githubusercontent.com/85003576/123544278-30767f00-d75b-11eb-8154-f0e1875a91cf.jpg)

