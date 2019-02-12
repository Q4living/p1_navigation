# Udacity DRLND Project 1 Navigation

## Learning Algorithm

The Algorithm used in this project is based on the vanila DQN from the coding exercise. It predicts an action value from the local network based on the env and action that the agent has acted. It also coupled with the vanila experience replay, so the agent can fine the local and target network based on their experience in the memory.

### Model architecture
2 fully connected dense layer with relu as the activation function

### Hyperparameters
1. fc1_units=64, activation=relu # Layer 1 neuron size and activation function
1. fc2_units=64, activation=relu # Layer 2 neuron size and activation function
1. BUFFER_SIZE = int(1e5) # replay buffer size
1. BATCH_SIZE = 64 # minibatch size
1. GAMMA = 0.99 # discount factor
1. TAU = 1e-3 # for soft update of target parameters
1. LR = 5e-4 # learning rate 
1. UPDATE_EVERY = 4 # how often to update the network

With above hyper parameter setting, the agent was able to achieve good performance and reach score 12 in 20 episodes.

## Plot of Rewards

![Plot of Rewards](p1_nav_score_plt_00.png)

[video link](https://youtu.be/bANBVKUrS0M)

## Ideas for Future Work

This simple DQN agent shows a common issue that it does not remember the state of the bananas it has seen. As such, the geo-location information is lost and the agent only pick up the most bananas it sees at the moment. Therefore, I will continue to work on it for a higher dimension that connect to the neural network to approximate distance and location of each object the agent has seen. Then, the agent can find optimal path to collect most of the bananas within the time period.

