## Navigation with DeepRL in a Unity environment

In this project, we train an agent to navigate in a large squared world. The goal is to collect yellow banana while avoiding the blue ones. A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:

- `0` - move forward.

- `1` - move backward.

- `2` - turn left.

- `3` - turn right.

The task is episodic, and in order to "solve" the environment, an agent must get an average score of +13 over 100 consecutive episodes.

### Files

- `dqn_agent.py` contains the agent and replay_buffer class.
the agent class as a doubleDQN bool argument that allow it to be a doubleDQN agent if set to true.
The replay_buffer class contains all the tuples (state, action, reward, next_state, done) yield during the training of the agent. They will be used to train it with fixed Q-targets.

- `model.py` contains the class QNetwork which is a fully connected deep network (it has three hidden layers). We used the relu activation function but others can apply.

- `Navigation.ipynb` is the notebook were you can test and train the agents.

### How to Install


### Results

It seems here that the DoubleDQN was not verry helpfull but that both of them were quit fast learner.
This graphics is an average of 12 agents of both "simple" and double DQN. Then in order to have a readable graphic, I have made an average of the 100 values before each episode. For exemple, for the 120th episode, we will average episode 20 to 120.

![DQN vs doubleDQN 12 agent & 650 episode window = 100](
        Navigation-with-DRL-in-a-Unity-environment/DQN vs doubleDQN 12 agent & 650 episode window = 100.png
      )

### Idea for later

It would be interesting to implement dueling DQN and prioritized replay to see whether it has more influence than doubleDQN on the Agent. Maybe should we launch a big simulation to see how each variable influence the learning time. Testing changes in the deep Network should be verry productive too.
