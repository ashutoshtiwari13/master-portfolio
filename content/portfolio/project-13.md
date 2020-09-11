---
title: "Unity Crawler Environment using Proximal Policy Optimization (PPO)"
date: 2019-05-12T12:14:34+06:00
image: "images/portfolio/item-13.gif"
client: "Ashutosh Tiwari"
project_url : "https://github.com/ashutoshtiwari13/Hands-on-DeepRL-and-DL"
categories: ["RL"]
description: "This is meta description."
draft: false
---

#### Project Heads-up

The [Crawler](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#crawler) environment. A creature with 4 arms and 4 forearms.   
Agent Reward Function (independent):
* +0.03 times body velocity in the goal direction.
* +0.01 times body direction alignment with goal direction.

<img src="https://github.com/ashutoshtiwari13/Unity-DRL-Hub/blob/master/Crawler-Env-PPO/output/crawler.png" height="425px" width="380px" hspace="20"/><img src="https://github.com/ashutoshtiwari13/Unity-DRL-Hub/blob/master/Crawler-Env-PPO/output/crawler.gif" height="425px" width="400px"/>

**Goal** : The agents must move its body toward the goal direction without falling.

CrawlerStaticTarget - Goal direction is always forward.
CrawlerDynamicTarget- Goal direction is randomized.

The Observation space consists of 117 variables corresponding to position, rotation, velocity, and angular velocities of each limb plus the acceleration and angular acceleration of the body. Vector Action space: (Continuous) Size of 20, corresponding to target rotations for joints.

The version of environment in this project contains 12 identical agents, each with its own copy of the environment.

Note : For details of PPO please see the summary of the PPO paper [here](https://github.com/ashutoshtiwari13/A-RL-Paper-A-Day-Keeps-boredom-away)


#### Click 👉 for [Project Details](https://github.com/ashutoshtiwari13/Unity-PyBullet-DRL-Hub/tree/master/Crawler-Env-PPO)
