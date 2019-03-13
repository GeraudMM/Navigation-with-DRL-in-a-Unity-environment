## Navigation with DeepRL in a Unity environment

In this project, we train an agent to navigate in a large squared world. The goal is to collect yellow banana while avoiding the blue ones. A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:

0 - move forward.

1 - move backward.

2 - turn left.

3 - turn right.

The task is episodic, and in order to "solve" the environment, an agent must get an average score of +13 over 100 consecutive episodes.
