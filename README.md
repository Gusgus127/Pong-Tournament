Part 1: Solving the Pong Environment

This part of the project implements and compares two reinforcement learning approaches, Deep Q-Networks (DQN) and REINFORCE, in the Atari Pong environment. The objective is to analyze the differences between a value-based and a policy-based method under the same experimental conditions.

The PongNoFrameskip-v4 environment from Gymnasium is used with standard Atari preprocessing, including frame skipping, grayscale conversion, resizing, frame stacking, and reward clipping. This ensures stable training and consistent observations for both agents.

The DQN agent learns an action-value function using a convolutional neural network, experience replay, a target network, and an ε-greedy exploration strategy. In contrast, the REINFORCE agent directly learns a stochastic policy using policy-gradient updates based on episode returns.

Both agents are evaluated after training in the same environment, and their performance is compared using episode rewards and observed gameplay behavior.

Part 2: Pong World Tournament

This part of the project focuses on training reinforcement learning agents in Atari environments using Stable-Baselines3. The goal is to leverage well-established implementations of reinforcement learning algorithms and compare their behavior with custom implementations from earlier parts of the project.

The experiments use Gymnasium Atari environments with standard preprocessing and wrappers to ensure stable training and consistent observations. Different algorithms provided by Stable-Baselines3 are trained and evaluated under the same conditions.

Agent performance is assessed using episode rewards and training curves. This part emphasizes practical aspects of reinforcement learning, such as algorithm selection, training stability, and reproducibility when using high-level reinforcement learning libraries.

Part 3: Solving a "complex" ALE environment

This part of the project explores multi-agent reinforcement learning in Atari environments using the PettingZoo framework. The objective is to extend single-agent reinforcement learning to a multi-agent setting and analyze how agents interact and learn within a shared environment.

The environment is built using PettingZoo’s Atari interfaces, with ALE as the backend. Standard preprocessing and environment transformations are applied using SuperSuit to ensure compatibility with learning algorithms and consistent observation spaces.

Training is performed using Stable-Baselines3, adapting single-agent algorithms to the multi-agent setup through environment wrappers. Agents are trained and evaluated based on episode rewards and observed interaction dynamics. Experiment tracking and logging are optionally handled using Weights & Biases (wandb).

This part highlights the challenges and differences between single-agent and multi-agent reinforcement learning, particularly in terms of environment design, training stability, and coordination.
