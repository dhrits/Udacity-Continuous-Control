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

### Installing requirements
In order to install requirements, please follow instructions provided at [Udacity's DRLND repository here](https://github.com/udacity/deep-reinforcement-learning#dependencies). A minimal set of instructions to install dependencies is listed below:

1. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```
	
2. Clone [this repository](https://github.com/udacity/deep-reinforcement-learning) (if you haven't already!), and navigate to the `python/` folder.  Then, install several dependencies.
```bash
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```
3. Follow **Getting Started** instructions at [Udacity's Navigation Project github page](https://github.com/udacity/deep-reinforcement-learning/tree/master/p2_continuous-control) to install the Unity Agents environment. These instructions are copy pasted below for convenience:
-  Download the environment from one of the links below.  You need only select the environment that matches your operating system:

    - **_Version 1: One (1) Agent_**
        - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
        - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

    - **_Version 2: Twenty (20) Agents_**
        - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
        - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
        - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
        - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux_NoVis.zip) (version 1) or [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux_NoVis.zip) (version 2) to obtain the "headless" version of the environment.  You will **not** be able to watch the agent without enabling a virtual screen, but you will be able to train the agent.  (_To watch the agent, you should follow the instructions to [enable a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md), and then download the environment for the **Linux** operating system above._)
   
4. Alternatively, you may also simply run the following command from **this repository's root**:
```
pip -q install ./python
```
_Note that while this has been tested in Udacity's workspace, you may encounter errors while running locally._ In this case, please follow instructions 1-3 to manually set up your dependencies. **Simply running the cells in ```Continuous-Control.ipynb```** will go through these steps.

### Training the agent
In order to train the agent, **please go through the training cells in** ```Continuous-Control.ipynb```. The result of the training are the checkpoint_actor.pth and checkpoint_critic.pth files which stores the weights of the trained actor and critic networks respectively. The notebook lists the step-by-step instructions to train these agents.

### Testing the agent
In order to test the agent, **please go through the testing cells in** ```Continuous_Control_Testing.ipynb```. Ensure that valid ```checkpoint_actor.pth``` and ```checkpoint_critic.pth``` files are present in the same folder as the notebook. My solution checkpoint is included in this repository. The cells in this notebook will run the agent in the environment. The agent easily achieves an average score of > 30 over 100 episodes. 

## Acknowledgments
The skeleton code for the deep-q-learning agent and associated model borrows heavily from [Udacity's example ```ddpg-pendulum``` agent lesson](https://github.com/udacity/deep-reinforcement-learning/tree/master/ddpg-pendulum). My solution builds on top of the provided files. Udacity Knowledge forums also had a wealth of advice from mentors who had answered existing questions (including advice to simplify the network).
