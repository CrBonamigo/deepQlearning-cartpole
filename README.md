
## About

> A pole is attached by an un-actuated joint to a cart, which moves along a frictionless track. The system is controlled by applying a force of +1 or -1 to the cart. The pendulum starts upright, and the goal is to prevent it from falling over. A reward of +1 is provided for every timestep that the pole remains upright. The episode ends when the pole is more than 15 degrees from vertical, or the cart moves more than 2.4 units from the center. [source](https://gym.openai.com/envs/CartPole-v0/)

## DQN
Standard DQN with Experience Replay.

### Hyperparameters:

* GAMMA = 0.95
* LEARNING_RATE = 0.001
* MEMORY_SIZE = 1000000
* BATCH_SIZE = 32
* EXPLORATION_MAX = 1.0
* EXPLORATION_MIN = 0.01
* EXPLORATION_DECAY = 0.995

### Model structure:

1. Dense layer - input: **4**, output: **24**, activation: **relu**
2. Dense layer - input **24**, output: **24**, activation: **relu**
3. Dense layer - input **24**, output: **2**, activation: **linear**

* **MSE** loss function
* **Adam** optimizer

##### Example trial chart

<img src="scores/scores.png">

##### Solved trials chart

<img src="scores/solved.png">

