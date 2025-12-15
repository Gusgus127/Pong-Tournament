Part 1: Pong Tournament – DQN and REINFORCE

This part of the project implements and compares two reinforcement learning approaches, Deep Q-Networks (DQN) and REINFORCE, in the Atari Pong environment. The objective is to analyze the differences between a value-based and a policy-based method under the same experimental conditions.

The PongNoFrameskip-v4 environment from Gymnasium is used with standard Atari preprocessing, including frame skipping, grayscale conversion, resizing, frame stacking, and reward clipping. This ensures stable training and consistent observations for both agents.

The DQN agent learns an action-value function using a convolutional neural network, experience replay, a target network, and an ε-greedy exploration strategy. In contrast, the REINFORCE agent directly learns a stochastic policy using policy-gradient updates based on episode returns.

Both agents are evaluated after training in the same environment, and their performance is compared using episode rewards and observed gameplay behavior.
