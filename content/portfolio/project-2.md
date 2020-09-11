---
title: "Image Segmentation using PCL"
date: 2020-04-12T12:14:34+06:00
image: "images/portfolio/item-2.png"
client: "Ashutosh Tiwari"
project_url : "https://github.com/ashutoshtiwari13/Hands-on-ROS-botics"
categories: ["Robotics"]
description: "This is meta description."
draft: false
---

#### Project Heads-up

The project creates a [ROS Node](http://wiki.ros.org/ROS/Tutorials/UnderstandingNodes) for image segmentation for objects kept on the cluttered table from the `pcd`'s used in the RANSAC plane fitting project above. The setup is run and tested on the RoboND simulator Environment provided by Udacity. The segmentation has been visualized in `Rviz` by selecting the `/pcl_objects` topic.
A successful implementation of the cluster based segmentation using [Voxel Grid filtering](https://python-pcl-fork.readthedocs.io/en/rc_patches4/tutorial/filtering.html#downsampling-a-pointcloud-using-a-voxelgrid-filter) results in assigning a different colour to each custer.

The `Gazebo` setup for the same table top consists of a stick robot with an RBG-D camera attached to its head.




#### Click 👉 for  [Project Details](https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation#Image-Segmentation)


<img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/sensor_stick/pcl1.png" height="425px" width="380px" hspace="20"/><img src="https://github.com/ashutoshtiwari13/ROS-PCL-Segmentation/blob/master/sensor_stick/pcl2.png" height="425px" width="400px"/>
