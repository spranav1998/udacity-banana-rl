# Report
## Navigation Using Deep Reinforcement Learning
By: Pranav S  
In this project, I, Pranav S., explored the field of Deep Reinforcement Learning (DRL), with a focus on utilizing a Deep Q Network (DQN) algorithm augmented with Prioritized Experience Replay (PER) to train an agent navigating a Unity-generated virtual environment [1][2][3].  
  
The agent was designed to operate in a vast, square world, with the goal of collecting yellow bananas while avoiding blue ones. This environment, known as the Banana Collector environment, provides an episodic task where the agent has to secure an average score of +13 over 100 consecutive episodes to be considered as having "solved" the environment.  
  
The implementation of the DQN algorithm involved designing a deep neural network, capable of generalizing past experiences to new ones, with two layers each containing 128 neurons. This network was utilized as a function approximator in the DQN algorithm, receiving a 37-dimensional state space vector from the environment and outputting an action for the agent to execute.  
  
The DQN, as introduced by [2], typically uses the Bellman equation for iterative updates to estimate the action-value function. However, the project incorporated two crucial improvements. Firstly, a soft update strategy was employed, making the target network slightly closer to the current network at each update. Secondly, the project utilized reward clipping, confining the reward between -1 and 1.  
  
To further enhance the learning process, Prioritized Experience Replay (PER) was incorporated into the DQN algorithm [3]. PER modifies the standard experience replay method by favoring experiences from which the agent can learn the most. This is done by increasing the replay probability of experiences that have a high expected learning progress, as measured by the absolute TD-error.  
  
The hyperparameters used were a buffer size of 100,000 experiences, a mini-batch size of 64, a discount factor of 0.99, and a learning rate of 0.0005. The Q-networks were updated every four steps.  
  
Using these techniques, the agent was able to achieve an average score of 13.1 in 515 episodes, effectively demonstrating the application and utility of DQN with PER in training agents to accomplish complex tasks in high-dimensional state spaces.  

## References:
[1] Unity-Technologies. Unity Machine Learning Agents Toolkit. https://github.com/Unity-Technologies/ml-agents  
[2] Mnih, V. et al., 2015. Human-level control through deep reinforcement learning. Nature, 518(7540), pp. 529–533.  
[3] Schaul, T., Quan, J., Antonoglou, I., & Silver, D. (2015). Prioritized Experience Replay. arXiv preprint arXiv:1511.05952.  
