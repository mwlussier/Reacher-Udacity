To resolve the project, a Deep Deterministic Policy Gradient (DDPG) was used.

The difference between a DDPG and a DQN model is the implementation of a second network known as critic. The first network, the actor, is used to approximate the optimal policy by always selecting the best believed action for any given state as the output. The critic network learns to evaluate the optimal action value function by using the actors best believed action.

Furthermore, a soft update function is applied to both the actor and critic network during their learning stage. This function blends a very small portion of the local network, which is the most up to date one, with the target network, which is the one we use for prediction to stabilize training.

An addition to the DDPG agent is the implementation of a noise function (Ornstein-Uhlenbeck process) during the action stage. This addition makes the model exploration process more robust. 
