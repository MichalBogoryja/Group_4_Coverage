# Group_4_Coverage

[TOC]

## Introduction

The aim of this project is to demonstrate multi-robot cooperation through a maze in the VREP simulation program. We are to make them perform a coverage task, one of two methods of terrain traversability.


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
3. Download VREP simulation from: http://coppeliarobotics.com/files/V-REP_PRO_EDU_V3_5_0_Linux.tar.gz
4. RVIZ - UserGuide of RVIZ: http://wiki.ros.org/rviz/UserGuide

## Running the system

In order to run the system, following steps are to be executed:

1. Run roscore in a terminal 

   ```bash
   $ roscore
   ```

2. Open a new Terminal & Run V-REP

   ```bash
   $ cd <VREP_folder_path>/
   ```

   ```bash
   $ ./vrep.sh
   ```

3. Open a new Terminal & Run the node operating RGB point cloud for the first robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch rgb_pcd_kinect_fusion rgb_pcd_kinect_fusion_turtlebot1.launch
   ```

4. Open a new Terminal & Run the node operating RGB point cloud for the second robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch rgb_pcd_kinect_fusion rgb_pcd_kinect_fusion_turtlebot2.launch
   ```
5. Open a new Terminal & Run the rviz

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch vrep_turtlebot_simulation vrep_turtlebot_rviz_launch.launch
   ```
6. Open a new Terminal & Run the node octomap for the first robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_robot_launchers vrep_octomap_turtlebot1.launch
   ```
7. Open a new Terminal & Run the node octomap for the second robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_robot_launchers vrep_octomap_turtlebot2.launch
   ```
8. Open a new Terminal & Run the node global mapping 

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch ms_vrep_ros_simulation global_mapping.launch
   ```
9. Open a new Terminal & Run the node normal estimation for the first robot

   ```bash
   $ cd coverage_ws
   ```

   ```bash
   $ source source_all.bash
   ```

   ```bash
   $ roslaunch turtlebot_robot_launchers turtlebot_normal_estimation_turtlebot1.launch
   ```
10. Open a new Terminal & Run the node normal estimation for the second robot

      ```bash
      $ cd coverage_ws
      ```

      ```bash
      $ source source_all.bash
      ```

      ```bash
      $ roslaunch turtlebot_robot_launchers turtlebot_normal_estimation_turtlebot2.launch
      ```
11. Open a new Terminal & Run the node turtlebot traversability analysis for the first robot

      ```bash
      $ cd coverage_ws
      ```

      ```bash
      $ source source_all.bash
      ```

      ```bash
      $ roslaunch turtlebot_robot_launchers turtlebot_traversability_analysis_turtlebot1.launch
      ```
12. Open a new Terminal & Run the node turtlebot traversability analysis for the second robot

      ```bash
      $ cd coverage_ws
      ```

      ```bash
      $ source source_all.bash
      ```

      ```bash
      $ roslaunch turtlebot_robot_launchers turtlebot_traversability_analysis_turtlebot2.launch
      ```
13. Open a new Terminal & Run the node path planner for the first robot

      ```bash
      $ cd coverage_ws
      ```

      ```bash
      $ source source_all.bash
      ```

      ```bash
      $ roslaunch turtlebot_robot_launchers turtlebot_path_planner_turtlebot1.launch
      ```
14. Open a new Terminal & Run the node path planner for the second robot

      ```bash
      $ cd coverage_ws
      ```

      ```bash
      $ source source_all.bash
      ```

      ```bash
      $ roslaunch turtlebot_robot_launchers turtlebot_path_planner_turtlebot2.launch
      ```
15. Open a new Terminal & Run the node keyboard_teleop for steering the first robots through arrow keys

      ```bash
      $ cd coverage_ws
      ```

      ```bash
      $ source source_all.bash
      ```

      ```bash
      $ roslaunch turtlebot_teleop_keyboard keyboard_teleop_diff_drive_mux_turtlebot1.launch
      ```
16. Open a new Terminal & Run the node keyboard_teleop for steering the second robots through arrow keys

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
Recchiuto, Carmine & Nattero, Cristiano & Sgorbissa, Antonio & Zaccaria, Renato. (2014). "Coverage Algorithms for Search and Rescue with UAV Drones - abstract" C. Nattero, C.T. Recchiuto, A. Sgorbissa, R. Zaccaria, PISA 10-12 Dicember 2014. 



## Authors

Michal Bogoryja-Zakrzewski 

Arnold Bukachi

Tengxiao He

Ishita Parekh

Haiwei Xu
