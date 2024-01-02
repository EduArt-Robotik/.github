# Welcome to EduArt's repository overview
On this page you will find the documentation of the software packages for our robots as well as project-related repositories.

## Actively maintained robot repositories
### edu_robot
General interface description for all EduArt robots. Docker images are available to control our robots.  
Link: [edu_robot](https://github.com/EduArt-Robotik/edu_robot)

### iotbot
ROS interface for the IOTBot. Description of the hardware interfaces. This repository is still up-to-date for a ROS-based installation. If you want to use ROS2, it is better to switch to edu_robot or iotbot-ros2.  
Link: [iotbot](https://github.com/EduArt-Robotik/iotbot)

### iotbot-ros2
ROS2 port of the iotbot repository.  
Link: [iotbot-ros2](https://github.com/EduArt-Robotik/iotbot-ros2)

## Perception repositories
This section contains higher-level algorithms that can be useful for (semi-)autonomous operation.
### edu_perception
Various software algorithms for the detection of objects. Only one QR code detector is currently implemented/referenced.  
Link: [edu_perception](https://github.com/EduArt-Robotik/edu_perception)
### edu_swarm
Extension package to control several robots synchronously.  
Prerequisite: All robots require a precise localization concept.  
Link: [edu_swarm](https://github.com/EduArt-Robotik/edu_swarm)

## Utility repositories
Useful tools for controlling our robots.
### edu_virtual_joy
Virtual joystick based on Python3. There is a version for ROS and ROS2, which can be used for all robots that process a message of type geometry_msgs/Twist.  
Link: [edu_virtual_joy](https://github.com/EduArt-Robotik/edu_virtual_joy)
### joystick_drivers
Forked from ros-drivers/joystick_drivers (Convinience copy)  
Link: [joystick_drivers](https://github.com/EduArt-Robotik/joystick_drivers)

## Project-related repositories
### edu_robocup_rescue_stack
Public benefit repository, that contains software that is useful for the RoboCup in the discipline of rescue robotics.  
Link: [edu_robocup_rescue_stack](https://github.com/EduArt-Robotik/edu_robocup_rescue_stack)
### robotsunite
This educational project promotes inter-school collaboration in a scenario similar to rescue. Each school develops an individual robot and challenging obstacles / tasks. No single robot can solve the given tasks alone. Thus, student teams from several schools must join forces.  
You can find our project wiki here: [Wiki](https://github.com/EduArt-Robotik/robotsunite/wiki)  
Link: [robotsunite](https://github.com/EduArt-Robotik/robotsunite)