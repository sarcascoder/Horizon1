![Banner](logo/horizon_banner.png)
### Applied Reinforcement Learning @ Facebook
[![Build Status](https://ci.pytorch.org/jenkins/buildStatus/icon?job=horizon-master)](https://ci.pytorch.org/jenkins/job/horizon-master/)
---

#### Overview

What is this project?
Horizon is an end-to-end platform for Applied Reinforcement Learning (RL) developed by Facebook (now Meta). It is designed for large-scale, production-level recommendation and optimization tasks where you don't have access to a simulator.

Where to Use This Project
Horizon is ideal for:

Use Case	Description
Recommendation Systems	Personalizing content, products, or ads based on user behavior
Ad Optimization	Deciding which ads to show to maximize engagement/revenue
Notification Optimization	Deciding when and what notifications to send
News Feed Ranking	Ranking posts based on user engagement
Game AI	Training agents to play games (OpenAI Gym environments)
Resource Allocation	Optimizing allocation decisions in business systems
Any Sequential Decision Making	Problems where actions affect future states and rewards
How to Use It
The workflow follows these steps:

Collect Data - Log interactions (state, action, reward, next_state) from your production system
Preprocess with Timeline - Convert data into consecutive (state, action, next_state) pairs using Apache Spark
Normalize Features - Automatically determine normalization parameters
Train Offline - Train RL models (DQN, DDPG, SAC) on batches of historical data
Evaluate with CPE - Use Counterfactual Policy Evaluation to estimate new policy performance
Deploy - Export model for serving with Caffe2
Input

Horizon is an open source end-to-end platform for applied reinforcement learning (RL) developed and used at Facebook. Horizon is built in Python and uses PyTorch for modeling and training and Caffe2 for model serving. The platform contains workflows to train popular deep RL algorithms and includes data preprocessing, feature transformation, distributed training, counterfactual policy evaluation, and optimized serving. For more detailed information about Horizon see the white paper [here](https://research.fb.com/publications/horizon-facebooks-open-source-applied-reinforcement-learning-platform/).

#### Algorithms Supported
- Discrete-Action [DQN](https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf)
- Parametric-Action DQN
- [Double DQN](https://arxiv.org/abs/1509.06461), [Dueling DQN](https://arxiv.org/abs/1511.06581), [Dueling Double DQN](https://arxiv.org/abs/1710.02298)
- [DDPG](https://arxiv.org/abs/1509.02971) (DDPG)
- [Soft Actor-Critic](https://arxiv.org/abs/1801.01290) (SAC)

#### Installation
Horizon can be installed via. Docker or manually. Detailed instructions on how to install Horizon can be found [here](docs/installation.md).

#### Usage
Detailed instructions on how to use Horizon can be found [here](docs/usage.md).


