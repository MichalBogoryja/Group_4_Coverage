# Group_4_Coverage

[TOC]

## Introduction

The aim of this project is to 



## System requirements

• Ubuntu 16.04 LTS (Xenial Xerus)
• ROS Kinetic  
• V-REP PRO EDU 3.5.0 Linux 64
• RVIZ


## Installation

Laptop with Linux: 

1. Install ROS kinetic - follow steps from: http://wiki.ros.org/kinetic/Installation/Ubuntu
2. Create a catkin workspace - follow steps from: 
   1. http://wiki.ros.org/catkin/Tutorials/create_a_workspace
   2. http://wiki.ros.org/catkin/Tutorials/CreatingPackage <instead of calling package "beginner_tutorials" call it "my_dynamixel">
3. 

## Running the system

In order to run the system, following steps are to be executed:

1. Run roscore in a terminal 

   ```bash
   $ roscore
   ```

2. Run V-REP

   ```bash
   $ cd <VREP_folder_path>/
   ```

   ```bash
   $ ./vrep.sh
   ```

3. Run the node operating RGB point cloud for the first robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch rgb_pcd_kinect_fusion rgb_pcd_kinect_fusion_turtlebot1.launch
   ```

4. Run the node operating RGB point cloud for the second robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch rgb_pcd_kinect_fusion rgb_pcd_kinect_fusion_turtlebot2.launch
   ```
5. open the rviz

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch vrep_turtlebot_simulation vrep_turtlebot_rviz_launch.launch
   ```
6. Run the node octomap for the first robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_robot_launchers vrep_octomap_turtlebot1.launch
   ```
7. Run the node octomap for the second robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_robot_launchers vrep_octomap_turtlebot2.launch
   ```
8. Run the node global mapping 

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch ms_vrep_ros_simulation global_mapping.launch
   ```
9. Run the node normal estimation for the first robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_robot_launchers turtlebot_normal_estimation_turtlebot1.launch
   ```
10. Run the node normal estimation for the second robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_robot_launchers turtlebot_normal_estimation_turtlebot2.launch
   ```
11. Run the node turtlebot traversability analysis for the first robot
   
   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_robot_launchers turtlebot_traversability_analysis_turtlebot1.launch
   ```
12. Run the node turtlebot traversability analysis for the second robot
    
   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_robot_launchers turtlebot_traversability_analysis_turtlebot2.launch
   ```
13. Run the node path planner for the first robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_robot_launchers turtlebot_path_planner_turtlebot1.launch
   ```
14. Run the node path planner for the second robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_robot_launchers turtlebot_path_planner_turtlebot2.launch
   ```
15. Run the node keyboard_teleop for steering the first robots through arrow keys

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_teleop_keyboard keyboard_teleop_diff_drive_mux_turtlebot1.launch
   ```
16. Run the node keyboard_teleop for steering the second robots through arrow keys

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_teleop_keyboard keyboard_teleop_diff_drive_mux_turtlebot2.launch
   ```


## Main references 



## Authors

Michal Bogoryja-Zakrzewski 

Arnold Bukachi

Tengxiao He

Ishita Parekh

Haiwei Xu
