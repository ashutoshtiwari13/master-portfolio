---
title: "Policy Gradient Methods"
date: 2020-04-13:14:34+06:00
image: "images/blog/post-2.jpeg"
description: "This is meta description."
draft: false
---

#Introduction
RL is concerned with a foundational issue of how an intelligent agent can learn to make a good __sequences of decisions__, in contrast to ML where we discuss mostly __one__ decision.
Three aspects -
- sequence of decisions
- degree of goodness of the decisions
- the learning associated with making good decisions

#Application Area -
- Atari games
- Educational games
- Robotics
- Healthcare
- NLP ,vision Optimization techniques

#Key aspects-
- Optimization :- Goal is to find the best strategy or optimal way to make decisions
- Delayed Consequences :- Decisions now can impact things much later , saving for retirement . How to form a causal relationship for the relationship you made in the past and the decisions you mak in future.
- Exploration:- Learning about the world by making decisions
- Generalization:-
A policy is a kind of mapping from past experiences to action. It is a worthy point to note that why we don't just pre-program a policy? because its becomes nontractable as the action space becomes huge!

_AI planning vs RL_ -
Optimization happens, Generalization happens, Delayed consequences happen, but exploration does not happen in Ai Planning
Eg- The go Game can be a planning problem . It takes the model of the how the world is , the rules of the game, we know the reward , hard part is computing what you should do given the model of the world , doesn't require exploration

_Supervised machine learning & Unsupervised ML vs RL_
Optimization happens, generalization happens, but no exploration and Delayed consequences in ML
eg- Doesn't involve exploration because in supervised learning you are given a dataset
, so the agent is not collecting information instead it has used the already have experience to classify.
Its typically making one decision, and not caring about whether a decision made now will affect the ones coming later.

_Imitation learning vs RL_
Follows everything but exploration does not happen in imitation learning, as we are learning from the experience of others, so instead of our agent to take experiences from the world it imitates another agent
In general, IL + RL is used to give promising results!

#Sequential Decision Making
- The goal is to maximize the _expected_ future rewards
- may require a balance between immediate and long term rewards
- may require strategic behavior to achieve high rewards

Each time step t ,
- Agent takes an action at.
- World updates the given action at, emits observation Ot and a reward Rt
- agent receives observation Ot and rewards Rt

#Markov Assumption -
We assume that the state used by the agent is sufficient statistics of history. In order to predict the future, you only need to know the current state of the environment.
The future is independent of the past given the present(if in the present one have the aggregate statistics )
Why is Markov assumption popular -
Because having a large action space may improve the richness of the representation but we will only have data point per state, and no repeating and we lack the number of similar occurrences or prior experiences that can help the agent learn. As the number of each state is only one and not a cluster or aggregation  
So we assume, the most recent observation the agent gets is the state, st=ot

#Types of Sequential Decision making processes -
1. Bandits - Idea is that the actions that are taken have no influence on the next observations. Eg - if a Ct 1 like an add on a website, and other Ct2 logs in, the choice of Ct2 Is mostly not influenced bu the choice of add click by CT1

2. MDP's and POMDP's - idea is that the actions can affect the state of the world, i.e future observations

3. How the world changes - Deterministic( given history and action, single observations and reward) and Stochastic (given history and action, many potential observation and rewards)

#RL Algorithm Components-
- __Model__ - representation of how the world changes in response to agents action
- __Policy__ - Policy ''pi'' determines how the agent chooses actions .mappings from states to actions.
- __Value functions__ -  expected discounted sum of future rewards under a particular policy ''pi''

#Types of RL agent
- __Model-based__ - The maintained in their representation of a direct model of how the world works. may or may not have a policy or a value function.
- __Model-free__ - have an explicit value function and a policy function and no model.

#Explorationa and Exploitation
In exploration, we are interested in looking at things we have never tried before o tried things that might have been bad, but could be good in the future.
In exploitation, we are trying things that are expected to be good given the past experience.
Eg - In the case of movies -
   Exploitation - watching a fav movie you have seen before
   Exploitation - watching a new movie

   In advertising,
  Exploitation - Show the most effective as so far
  Exploration  - Show a new/different add
