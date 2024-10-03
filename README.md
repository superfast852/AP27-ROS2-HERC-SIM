
# Apolo 27's NASA HERC Obstacle Simulation for RC Division

This repository contains a Gazebo simulation of NASA's Human Exploration Rover Challenge (HERC) obstacles, scaled to the RC specs under the Handbook provided. This project aims to determine the behavior of the rover under the adverse conditions of the field.

## Table of Contents
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Simulation](#running-the-simulation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

---

## Overview
This project simulates the obstacles from NASA's HERC competition, enabling teams to practice and refine their rover control strategies. The environment (as planned) includes:
- Rough terrains and materials
- Strategically placed obstacles
- Craters and inclines
- Crevasses and other terrains

## Prerequisites
Ensure you have the following installed:
- **ROS 2 (Foxy, Humble, or Rolling)**
- **Gazebo (Garden or compatible versions)**
- **colcon build system**
- **Python 3.8+**

To install ROS 2 and Gazebo, follow the official setup guides:
- [ROS 2 installation guide](https://docs.ros.org/en/foxy/Installation.html)
- [Gazebo installation guide](https://gazebosim.org/docs)

## Installation
This assumes you have installed Gazebo (Ignition) and ROS2 before.
First, CD to the ros2 workspace, and run the following commands:

```
colcon build
source install/setup.bash
```
Now, you should be ready to go!

## IMPORTANT:
This project runs on the Ignition version of gazebo, using Citadel (gz), Foxy (ROS2), and Focal (Ubuntu). Please change the code according to your own options.

## Running the Simulation
First, setup the bridge between ROS2 and Gazebo:
```
ros2 run ros_ign_bridge parameter_bridge /cmd_vel@geometry_msgs/msg/Twist@ignition.msgs.Twist
```
This sets up a bridge on cmd_vel for communicating ros with the simulation.

Then, just run your gazebo simulation with:
```
ign gazebo building_robot.sdf -v4
```

## Usage
It's as simple as using the right trigger, and right joystick of the controller to drive.


## License
This project is licensed under the [MIT License](LICENSE).

---

