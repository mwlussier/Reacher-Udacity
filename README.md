# Reacher-Udacity
The objectif of this project is to train an agent to move a double-jointed arm to target locations.

The project environment is [Unity ML-Agents Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher).
Two separate versions of the Unity environment is provided by Udacity:
- containing a single agent
- containing 20 identical agents, each with its own copy of the environment

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location.

The state space has 33 variables and contains the agent's position, rotation, velocity, and angular velocities of the arm.
Each action is a vector with four values, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

In order to solve the environment, depending on the version, 

1. Single agent: the agent must get an average score of +30 over 100 consecutive episodes.
2. Multiple agents (20): the agents must get an overall average score of +30 over 100 consecutive episodes.


