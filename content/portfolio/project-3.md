---
title: "PR2-Robot 3D Perception and Control"
date: 2019-05-12T12:14:34+06:00
image: "images/portfolio/item-3.jpg"
client: "Ashutosh Tiwari"
project_url : "https://github.com/ashutoshtiwari13/Hands-on-ROS-botics"
categories: ["Robotics","RL"]
description: "This is meta description."
draft: false
---

## Project Heads-up

This project gives the [PR2 robot](https://robots.ieee.org/robots/pr2/) the ability to locate an object in a cluttered environment, pick it up and then move it to some other location. This is an interesting problem to solve and is a challenge at the forefront of the robotics industry today. The project uses a perception pipeline , [here](https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation#Image-Segmentation) and [here](https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation#Object-Recognition-and-Labelling), to identify target objects from a so-called “Pick-List” in that particular order, pick up those objects and place them in corresponding drop-boxes.

Performing image segmentation and object detection are two important parts of the project forming the perception pipeline for the PR2 Robot. The control/Actuator part is handled by calling a `PR2 mover function`, which then calls the `pr2_mover` to pick and place detected objects.
The project deals with three test world scenarios one of whose results is shown in the below image


#### Project Details


#### Click 👉 for  [Project Details](https://github.com/ashutoshtiwari13/PR2Robot-3D-Perception)

<img src="https://github.com/ashutoshtiwari13/PR2Robot-3D-Perception/blob/master/pr2_robot/run/world1.jpg" height="350px" width="380px" hspace="20"/><img src="https://github.com/ashutoshtiwari13/PR2Robot-3D-Perception/blob/master/pr2_robot/run/obj2.png" height="350px" width="380px"/>


<img src="https://github.com/ashutoshtiwari13/PR2Robot-3D-Perception/blob/master/pr2_robot/run/world3.jpg" height="350px" width="380px" hspace="20"/><img src="https://github.com/ashutoshtiwari13/PR2Robot-3D-Perception/blob/master/pr2_robot/run/obj3.png" height="350px" width="380px"/>
