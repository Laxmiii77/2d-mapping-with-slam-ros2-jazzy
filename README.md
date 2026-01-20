# 🗺️ 2D SLAM Mapping with ROS 2 Jazzy

<image src=image.png/>
  
## 📌 Features

Real-time 2D occupancy grid mapping
LiDAR-based SLAM
Works in simulation (Gazebo) and real robots
Compatible with Nav2 for navigation
Clean launch and parameter structure

## 🧰 Tech Stack
ROS 2 Jazzy Jalisco
SLAM Toolbox (async / sync mode)
Gazebo (simulation)
LiDAR sensor (2D)
RViz2 (visualization)

## ⚙️ Prerequisites
Ubuntu 24.04
ROS 2 Jazzy installed
colcon build tools
Gazebo Harmonic / Classic
RViz2

## Install SLAM Toolbox for Jazzy
```bash
sudo apt update
sudo apt install ros-jazzy-slam-toolbox
```

## Clone the repository into the source directory of your workspace
``` bash
cd ros2_ws/src
git clone https://github.com/Laxmiii77/2d-mapping-with-slam-ros2-jazzy
```
## Launch the gazebo world simulation with obstacles
```bash
ros2 launch my_robot_description gazebo_with_obstacles.launch.py
```
## Launch the robot
```bash
ros2 launch my_robot_description robot_gazebo.launch.py
```
## Launch SLAM with parameter file
```bash
ros2 launch slam_toolbox online_async_launch.py \
slam_params_file:=/absolute/path/to/mapper_params.yaml
```
## Open Rviz2
```bash
rviz2
```
