---
title: "Introduction to Open Gym AI"
date: 2020-04-12T12:14:34+06:00
image: "images/blog/post-1.png"
description: "This is meta description."
draft: false
---

Understand the basic goto concepts to get a quick start on reinforcement learning and learn to test your algorithms with OpenAI gym to achieve research centric reproducible results.
This article first walks you through the basics of reinforcement learning and its current advancements. After, that we get dirty with code and learn about OpenAI Gym a tool often used by researchers for standardization and benchmarking results. When coding section comes please open your terminal and get ready for some hands on.



#### What’s Different here ?

Mainly three categories of learning are supervised, unsupervised and reinforcement. Let’s see basic differences b/w them. In supervised learning we try to predict a target value or class where the input data for training is already having labels assigned to it. Where as unsupervised learning uses unlabelled data for looking at patterns to make clusters, PCA or anomaly detection. RL algorithms are optimization procedures to find best methods to earn maximum reward i.e. give winning strategy to attain objective.

#### Hands On: Why OpenAI gym ?

> A 2016 Nature survey indicated that more than 70 percent of researchers have tried and failed to reproduce another scientist’s experiments, and more than half have failed to reproduce their own experiments.

OpenAI is created for removing this problem of lack of standardization in papers along with an aim to create better benchmarks by giving versatile numbers of environment with great ease of setting up. Aim of this tool is to increase reproducibility in the field of AI and provide tools with which everyone can learn about basics of AI.

What is OpenAI gym ? This python library gives us huge number of test environments to work on our RL agent’s algorithms with shared interfaces for writing general algorithms and testing them. Let’s get started just type pip install gym on terminal for easy install, you’ll get some classic environment to start working on your agent. Copy the code below and run it, your environment will get loaded only classic control comes as default. You can checkout other environments like Algorithmic, Atari, Box2D and Robotics [here](https://gym.openai.com/envs/).

      import gym
      env = gym.make('Acrobot-v1')
      env.reset()
      for _ in range(500):
           env.render()
           env.step(env.action_space.sample())
      from gym import envs
      print(envs.registry.all())`


When object interacts with environment with an action then step(…) function returns `observation` which represents environments state, `reward` a float of reward in previous action, `done` when its time to reset the environment or goal achieved and `info` a dict for debugging, it can be used for learning if it contains raw probabilities of environment’s last state. See how it works. Also, observe how `observation` of type `Space` is different for different environments.

      import gym
      env = gym.make('MountainCarContinuous-v0') # try for different environements
      observation = env.reset()
      for t in range(100):
              env.render()
              print observation
              action = env.action_space.sample()
              observation, reward, done, info = env.step(action)
              print observation, reward, done, info
              if done:
                  print("Finished after {} timesteps".format(t+1))
                  break[Output For Mountain Car Env:]
      [-0.56252328  0.00184034]
      [-0.56081509  0.00170819] -0.00796802138459 False {}[Output For CartPole Env:]
      [ 0.1895078   0.55386028 -0.19064739 -1.03988221]
      [ 0.20058501  0.36171167 -0.21144503 -0.81259279] 1.0 True {}
      Finished after 52 timesteps

What is `action_space` in above code? action-space & observation-space describes what is the valid format for that particular env to work on with. Just take a look at values returned.


      import gym
      env = gym.make('CartPole-v0')
      print(env.action_space) #[Output: ] Discrete(2)
      print(env.observation_space) # [Output: ] Box(4,)
      env = gym.make('MountainCarContinuous-v0')
      print(env.action_space) #[Output: ] Box(1,)
      print(env.observation_space) #[Output: ] Box(2,)


Discrete is non-negative possible values, above 0 or 1 are equivalent to left and right movement for CartPole balancing. Box represent n-dim array. These can help in writing general codes for different environments. As we can simply check the bounds env.observation_space.high/[low] and code them into our general algorithm.


#### Conclusion

Now, with the above tutorial you have the basic knowledge about the gym and all you need to get started with it. Gym is also TensorFlow compatible but I haven’t used it to keep the tutorial simple. After trying out gym you must get started with baselines for good implementations of RL algorithms to compare your implementations. To see all the OpenAI tools check out their [github](https://github.com/openai) page. RL is an expanding fields with applications in huge number of domains and it will play an important role in future AI breakthroughs. Thanks for reading!!
