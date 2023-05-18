# udacity-banana-rl
In this project, a reinforcement learning agent is trained to navigate and collect bananas within a large, square world. The agent utilizes an implementation of the Deep Q-Network (DQN) algorithm for training, designed using the Unity Machine Learning Agents Toolkit.

The simulated environment is a variation of Unity's Banana Collector, adjusted for Udacity's Deep Reinforcement Learning Nanodegree. The agent's objective is to gather as many yellow bananas as possible while evading blue bananas.

Problem Statement
The agent receives a reward of +1 for collecting a yellow banana, and a reward of -1 for collecting a blue banana. The state space, comprising 37 dimensions, contains the agent’s velocity and a ray-based perception of objects around its forward direction.

The agent can perform four discrete actions:

0 - Move forward.
1 - Move backward.
2 - Turn left.
3 - Turn right.

The task is episodic. To successfully solve the environment, the agent must achieve an average score of +13 over 100 consecutive episodes.

Implementation
Our DQN Agent utilizes a Neural Network with three fully connected layers. PyTorch framework is used for the implementation of this network. We have also incorporated epsilon-greedy strategy for action selection, and a buffer memory of size 10000 is used for experience replay.

To run this project, the following Python libraries are required:

NumPy
PyTorch
UnityAgents
Execution
Navigate to the top-level project directory udacity-banana-rl/ (which contains this README) and run the following command:

sh
Copy code
$ jupyter notebook
This will open the Jupyter Notebook software and notebook in your browser, enabling you to explore and reproduce the experiments that have been run.

References
Schaul, T., Quan, J., Antonoglou, I., & Silver, D. Prioritized Experience Replay. arXiv.org, 2015.
Van Hasselt, H., Guez, A., & AAAI, D. S. Deep Reinforcement Learning with Double Q-Learning. Aaai.org, 2016.
Mnih, V., Kavukcuoglu, K., Silver, D., Rusu, A. A., Veness, J., Bellemare, M. G., et al. Human-level control through deep reinforcement learning. Nature, 52015.
