# PiCar-QRMultiMapping

## Project Overview:

_TBD_

## Installation Requirements

- _ROS Version_ Required: Noetic on Ubuntu 20.04

Follow the ufficial procedure at [ROS Noetic](http://wiki.ros.org/noetic/Installation/Ubuntu)

- Make sure that _Gazebo_ and _Rviz_ are installed:

```bash
sudo apt-get install ros-noetic-gazebo-ros-pkgs ros-noetic-gazebo-ros-control
```

```bash
sudo apt-get install ros-noetic-rviz
```

## Installation Steps

### TurtleBot Environment

For the first development it is necessary the TurtleBot environment.

Follow the ufficial procedure at [Gazebo Simulation](https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/#gazebo-simulation) and change _catkin_ws_ with _turtle_ws_

Make sure to add

```bash
export TURTLEBOT3_MODEL=waffle
```

to your _.bashrc_ file

Remember to source this workspace by adding

```bash
source ~/turtle_ws/devel/setup.bash
```

to your _.bashrc_ file

### Vision Visp

For the detection of the various QR codes it is necessary the package [ViSP stack for ROS](https://github.com/lagadic/vision_visp/tree/noetic)

Follow the ufficial procedure at [vision_visp](http://wiki.ros.org/vision_visp)(probably it will be neccesary to install from source, remember that the workspace is called _turtle_ws_)

In order to try the correct installation, run

```bash
roslaunch visp_auto_tracker tutorial.launch
```

### QR-code Maker

#### 1. Copy the existing Arena

In order to display the correct QR codes in the TurtleBot environment, copy and past the folder

```bash
turtle_ws/src/turtlebot3_simulations/turtlebot3_gazebo/worlds
turtle_ws/src/turtlebot3_simulations/turtlebot3_gazebo/models
turtle_ws/src/turtlebot3_simulations/turtlebot3_gazebo/launch
```

into your workspace at the defined positions. In this way you will obtain the QR codes positioned in the TurtleBot Arena.

#### 2. Creake QR codes form scratch

_TODO_

### Try the installaion

To try the correct installation run

```bash
roslaunch turtlebot3_gazebo turtlebot3_visp_world.launch
```

and in a different terminal, in order to move he robot

```bash
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
