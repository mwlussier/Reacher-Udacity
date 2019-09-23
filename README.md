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

1. *Single agent (1):* The agent must get an average score of +30 over 100 consecutive episodes.
2. *Multiple agents (20):* The agents must get an overall average score of +30 over 100 consecutive episodes.

------

Follow the instructions below to be able to run the code.

## Step 1: Clone the DRLND Repository
Follow the instructions in the [DRLND GitHub](https://github.com/udacity/deep-reinforcement-learning#dependencies) repository to set up the Python environment. These instructions can be found in **README.md** at the root of the repository. By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.

## Step 2: Download the Unity Environment
It is not needed to install Unity - you can download the environment provided by Udacity from one of the links below. You only need to select the environment that matches your operating system:

*Version 1: One (1) Agent*
  * Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
  * Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
  * Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
  * Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

*Version 2: Twenty (20) Agents*
  * Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
  * Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
  * Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
  * Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

Then, place the file in the _p2_continuous-control/_ folder in the DRLND GitHub repository, and unzip (or decompress) the file.

------

To train the agent, follow the steps in Reacher_Continuous_Control.ipynb

To see the agent perform in the environment, follow the steps in Reacher_Continuous_Control_test.ipynb

