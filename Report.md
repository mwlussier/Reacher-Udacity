## Reacher Project

To resolve the project, a **Deep Deterministic Policy Gradient** (DDPG) was used.

The main difference between a DDPG and a **Deep Q Network** (DQN) model is the implementation of a second network known as critic.
1. The first network, the actor, will take the state **s** as input and returns the action **a** as output. It is used to approximate the optimal policy by always selecting the best believed action for any given state as the output.

2. The critic network will take the state, action tuple **(s,a)** as input and returns the **Q-values** as output. It learns to evaluate the optimal action value function by using the actors best believed action.

Furthermore, a soft update function is applied to both the actor and critic network during their learning stage. This function blends a very small portion of the local network, which is the most up to date one, with the target network, which is the one we use for prediction to stabilize training.

An addition to the DDPG agent is the implementation of a noise function (Ornstein-Uhlenbeck process) during the action stage. This addition makes the model exploration process more robust and is trivial for the performance of the DDPG. As we will see, the performance of the agent is highly dependent to the variation of the sigma factor in the noise function.

The model architecture include for both actor and critic networks, three (3) fully connected layers and one (1) batch normalization layer between the first and the second layer. We are using a ReLu activation function for the two (2) first fully connected layers and a tangent function for the last one (only in the Actor network).

The batch normalization is used to apply a normalization process to the outputs of a previous layer such as it's done during the preprocessing phase of the initial data. This should increase the stability of the network and accelerate the learning process. Batch normalization is used with its default variables.

## Result
The architecture is construct to resolve the first version which is the single agent environment.
The best model achieved an average score of 37.21 after 400 episodes of training. It achieved an average score of 30.0 or more at best 200 episodes. The hyperparameters used are as follow:

* BUFFER_SIZE:  1e6
* BATCH_SIZE:   64
* GAMMA:        0.99
* TAU:          1e-3
* LR_ACTOR:     2e-4
* LR_CRITIC:    2e-4
* WEIGHT_DECAY: 0
* THETA:        0.15
* SIGMA:        0.05

For both Actor and Critic network:
* FC1_UNITS:    64
* FC2_UNITS:    128

![alt text](https://github.com/mwlussier/Reacher-Udacity/blob/master/images/reacher_ddpg_END.png)


As we can see in the following charts (which are only of 100 episodes for searching purpose), the best initial performance of the model is when SIGMA noise parameter is at 0.10. *(Only SIGMA variable was changed)*

1. SIGMA: 0.20

![alt text](https://github.com/mwlussier/Reacher-Udacity/blob/master/images/reacher_ddpg_sigma020.png)

2. SIGMA: 0.15

![alt text](https://github.com/mwlussier/Reacher-Udacity/blob/master/images/reacher_ddpg_sigma015.png)

3. SIGMA: 0.10

![alt text](https://github.com/mwlussier/Reacher-Udacity/blob/master/images/reacher_ddpg_sigma010.png)

4. SIGMA: 0.05

![alt text](https://github.com/mwlussier/Reacher-Udacity/blob/master/images/reacher_ddpg_sigma005.PNG)


## Future Work
* The natural amelioration would be to resolve the project using the multiple agents environment (20) with the same algorithm. 
* Furthermore, we could implement algorithms like PPO, A3C and D4PG that use multiple (non-interacting, parallel) copies of the same agent to distribute the task of gathering experience to resolve the second version.
