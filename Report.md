
# Project Report 2: Continuous Control

### Introduction
This report summarizes my attempt at solving the Continous Control project for the Udacity Reinforcement Learning Nanodegree. I had first attempted to solve the version 2 of the environment with 20 identical agents. But the leaning process was too long and even after two weeks of effort, I count not get the agent successfully trained. Hence, I choose to attempt the version 1 of the environment as the learning process is much faster giving me more time to experiment and tweak the network and learning parameters.

### Hyperparameters
- Replay buffer size 1e6
- Mini batch size 128
- TAU for soft update of target parameters 1e-3
- Learning rate 1e-4 for actor and 1e-4 for critic
- Ornstein-Uhlenbeck noise
- L2 weight decay = 0.0
- Discount factor = 0.99

### Actor Critic Model
The network comprises of 2 networks:
Actor: 128 -> 128
Critic: 128 -> 128
Batch normalization after the first and second hidden layers in both the Actor and Critic Networks.


### Results
The environment could be solved in ~250 episodes. From the chart, it looks like the the scores were increasing linearly till ~120 episodes after which the scores start to increase at a higher rate and then flatten after ~22 eposodes with scores fluctuating between 33 and 39. The wonwored score over last 100 episodes managed to cross a score of 30 after exactly 249 episodes.

### Further Improvements
- Solving the Version 2 of the environment with 20 identical agents
- Try to find out why the scores flatten after 220 episodes and try to get the agent score more than 50.
