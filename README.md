## Navigation with DeepRL in a Unity environment

### Environment

In this project, we train an agent to navigate in a large squared world. The goal is to collect yellow banana while avoiding the blue ones. A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:

- `0` - move forward.

- `1` - move backward.

- `2` - turn left.

- `3` - turn right.

The task is episodic, and in order to "solve" the environment, an agent must get an average score of +13 over 100 consecutive episodes.

## Files

- `dqn_agent.py` contains the agent and replay_buffer class.
The replay_buffer class contains all the tuples (state, action, reward, next_state, done) yield during the training of the agent. They will be used to train it with fixed Q-targets.

- `model.py` contains the class QNetwork which is a fully connected deep network (it has two hidden layers). We used the relu activation function but others can apply.

- `Navigation_2.ipynb` is the notebook were you can test and train the agents.

## Installing
 
To install the dependencies in order to create a virtual environment, follow the instructions bellow:

1 - Create (and activate) a new environment with Python 3.6.
(You can replace drlnd by what you want)

- Linux or Mac:
```
conda create --name drlnd python=3.6 
source activate drlnd
```
- Windows:
```
conda create --name drlnd python=3.6 
activate drlnd
```

2 - Go to the python folder and install the dependencies on your virtual environment:

```
cd python
pip install .
```

3 - To run the code on the notebook you need to create an IPython kernel for this virtual environment:

```
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```
 
 ### Unity Environment
 
To run the environment you will need to:

1 - Download the unity files from here:

- Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
- Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
- Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
- Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

2 - Place the file in the p1_navigation/ folder in the DRLND GitHub repository, and unzip (or decompress) the file.

### Training

Now you should be ready to run `Navigation_2.ipynb` and train your first agent.
