<img src="udacity_banner.jpg" height ="20">

### Robotics Software Engineer - Nanodegree

# Project 03 (of 05) : Where Am I
## Directory Structure
```
.Where_Am_I
   ├── my_robot
   │   ├── CMakeLists.txt
   │   ├── config
   │   │   ├── base_local_planner_params.yaml
   │   │   ├── costmap_common_params.yaml
   │   │   ├── global_costmap_params.yaml
   │   │   ├── local_costmap_params.yaml
   │   │   └── __MACOSX
   │   ├── launch
   │   │   ├── amcl.launch
   │   │   ├── robot_description.launch
   │   │   └── world.launch
   │   ├── maps
   │   │   ├── my_map.pgm
   │   │   └── my_map.yaml
   │   ├── meshes
   │   │   └── hokuyo.dae
   │   ├── package.xml
   │   ├── urdf
   │   │   ├── my_robot.gazebo
   │   │   └── my_robot.xacro
   │   └── worlds
   │       ├── empty.world
   │       └── my_world.world
   ├── pgm_map_creator
   │   ├── CMakeLists.txt
   │   ├── launch
   │   │   └── request_publisher.launch
   │   ├── LICENSE
   │   ├── maps
   │   │   └── map.pgm
   │   ├── msgs
   │   │   ├── CMakeLists.txt
   │   │   └── collision_map_request.proto
   │   ├── package.xml
   │   ├── README.md
   │   ├── src
   │   │   ├── collision_map_creator.cc
   │   │   └── request_publisher.cc
   │   └── world
   │       ├── my_world.world
   │       └── udacity_mtv
   ├── teleop_twist_keyboard
   │   ├── CHANGELOG.rst
   │   ├── CMakeLists.txt
   │   ├── package.xml
   │   ├── README.md
   │   └── teleop_twist_keyboard.py
   ├── LICENSE
   ├── README.md
   │
```

## Project Goals

## Output 

## Setup and run
Note: The commands in this README work, considering that the main workspace is located at ```/home/robond/workspace/catkin_ws/src```      
      Notice the ```robond``` username. Make appropriate changes for your system.
      
Warning: Some minor features will not work in your system if your username of the system is different.

[Click here for the fix and to learn more](#Missing-minor-feature)
#### 1. Update the Workspace image
```
$ sudo apt-get update && sudo apt-get upgrade -y 
```
### 2. Install supporting packages
```
$ sudo apt-get install ros-kinetic-navigation
$ sudo apt-get install ros-kinetic-map-server
$ sudo apt-get install ros-kinetic-move-base
$ sudo apt-get install ros-kinetic-amcl
```

OR

```
$ sudo apt-get install ros-kinetic-navigation && sudo apt-get install ros-kinetic-map-server && sudo apt-get install ros-kinetic-move-base && sudo apt-get install ros-kinetic-amcl
```
Replace ```kinetic``` with ```YOUR_DISTRO```
#### 3. Clone the files in /home/workspace
```
$ cd /home/robond/workspace/catkin_ws/src
$ git clone https://github.com/Avadhoot94/Where_Am_I.git
```
#### 4. Create a build directory and compile the code
```
$ cd /home/robond/workspace/catkin_ws
$ catkin_make
$ source devel/setup.bash
````
#### 5. Launch the world and the robot
```
$ roslaunch my_robot world.launch
```
Make sure the ```fixed frame``` in ```RViz``` is ```odom```
       
#### 6. Launch the AMCL package 
```
$ roslaunch my_robot amcl.launch
```
