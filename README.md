# DQN-Navigation-Project

This repository contains a project for Udacity deep reinforcement learning nanodegree. A deep Q-network based agent learns to collect bananas.

## The environment

### Summary

The environment consists of a square world with yellow and blue bananas, where the agent moves in a 2 dimensional (horizontal) plane. The agent's goal is to collect yellow bananas and avoid blue bananas. The episodes are limited in time.

### Dynamics

Yellow and blue bananas appear randomly in the environment. The agent moves on a 2D horizontal plane, and can collect the bananas simply by moving into them. The movement of the agent is bounded by a square wall that surrounds the accessible world.

### Rewards

The agent receives a +1 reward whenever it manages to collect a yellow banana, and a -1 reward whenever it collects a blue banana.

### Observations

Although a first person view of the world is provided for a visualisation of the environment for humans, the agent's observation space is not this image. The agent's observation space is a 37 dimensional vector, which according to the description of the task contains the agent's velocity, and ray based perception of objects around the agent's forward direction. In this project I will attempt to train an agent that uses an artificial neural network (ANN) to process the observations, without any a priori knowledge of finer details of the observation space.

### Actions

At each time step, the agent has to choose between four actions: move forward (action 0), move backward (action 1), turn left (action 2), and turn right (action 3).

### Solving the environment

The environment is considered solved when the agent achieves an average score of +13 over 100 consecutive episodes. By convention we say the agent solved the environment on the timestep N if timesteps N + 1 to N + 100 are the ones whose average first reaches this goal.

## Dependencies

This project has three groups of dependencies: IPython Jupyter notebooks, Python libraries used by the agent and the learning algorithm, and the Unity ML Agents environment described above.

### Unity Environment

This project is based on a pre-built Unity Envoronment for the agent. This is supplied by Udacity at the following locations depending on operating system:

- [Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
- [Mac OSX](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
- [Windows (32-bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
- [Windows (64-bit)](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

Extract this package into the project directory.

### Jupyter Environment

In order to use the code in this repository locally, you need a Jupyter installation. Follow installation instructions at [https://jupyter.org/install](https://jupyter.org/install).

Alternatively, if you have access to the Udacity environment set up for this project in the deep reinforcement learning nanodegree, this environment can be used. It also contains the Unity Environment preinstalled. This is the setup I actually used for developing the project.

### Python dependencies

The solution depends on the following packages:
 - unityagents
 - numpy
 - pytorch
 - tensorflow
 - matplotlib

These can be installed with pip using the supplied requirements.txt file in the `python` folder.

## How to run this code

The code to define and train the agent is included in the interactive Python notebook [Report.ipynb](Report.ipynb). To train the model from scratch, execute each code cell in the notebook in order. To evaluate a pre-trained model, create an agent and replace network weights with ones loaded from [checkpoint.pth](checkpoint.pth).
