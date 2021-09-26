 ## Introduction
 ### The Environment
The description of this environment is taken from the Udacity Continous Control lecture. In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

**This project solves the first version of the environment with a single agent**



### State Space
The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.


### Success criteria
The task is episodic, and in order to solve the environment, your agent must get an average score of +30 over 100 consecutive episodes.

## Getting started
Please follow the instructions to get started at [Udacity's Navigation Project github page](https://github.com/udacity/deep-reinforcement-learning/tree/master/p2_continuous-control). **Alternatively, if executing the project in a Udacity workspace, it is sufficient to run the notebooks which will install all relevant requirements via pip inline in the notebooks.**

### Training the agent
In order to train the agent, **please go through the training cells in** ```Continuous-Control.ipynb```. The result of the training are the checkpoint_actor.pth and checkpoint_critic.pth files which stores the weights of the trained actor and critic networks respectively. The notebook lists the step-by-step instructions to train these agents.

### Testing the agent
In order to test the agent, **please go through the testing cells in** ```Continuous_Control_Testing.ipynb```. Ensure that valid ```checkpoint_actor.pth``` and ```checkpoint_critic.pth``` files are present in the same folder as the notebook. My solution checkpoint is included in this repository. The cells in this notebook will run the agent in the environment. The agent easily achieves an average score of > 30 over 100 episodes. 

## Acknowledgments
The skeleton code for the deep-q-learning agent and associated model borrows heavily from [Udacity's example ```ddpg-pendulum``` agent lesson](https://github.com/udacity/deep-reinforcement-learning/tree/master/ddpg-pendulum). My solution builds on top of the provided files. Udacity Knowledge forums also had a wealth of advice from mentors who had answered existing questions (including advice to simplify the network).