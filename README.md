## Part 1: Solving the Pong Environment

This part of the project implements and compares two reinforcement learning approaches, Deep Q-Networks (DQN) and REINFORCE, in the Atari Pong environment. The objective is to analyze the differences between a value-based and a policy-based method under the same experimental conditions.

The PongNoFrameskip-v4 environment from Gymnasium is used with standard Atari preprocessing, including frame skipping, grayscale conversion, resizing, frame stacking, and reward clipping. This ensures stable training and consistent observations for both agents.

The DQN agent learns an action-value function using a convolutional neural network, experience replay, a target network, and an ε-greedy exploration strategy. In contrast, the REINFORCE agent directly learns a stochastic policy using policy-gradient updates based on episode returns.

Both agents are evaluated after training in the same environment, and their performance is compared using episode rewards and observed gameplay behavior.

## Part 2: Pong World Tournament
Part 2 focuses on **multi-agent reinforcement learning** using the
**PettingZoo** framework and its **AEC (Agent Environment Cycle) API**.
The goal is to train an agent capable of competing in a Pong tournament against
other agents.

Training is performed using **Stable-Baselines3 (PPO)** in a single-agent
Gymnasium Pong environment for efficiency and stability. The trained policy is
then transferred to the **PettingZoo Pong environment**, where it controls one
paddle in a two-player setting.

Preprocessing and observation transformations are applied using **SuperSuit**
to ensure consistency between the training and evaluation environments.
The agent is evaluated against a random opponent over multiple episodes,
reporting win rates, rewards, and gameplay videos, and is fully compatible
with the Pong World Tournament setup.

## Part 3: Solving a "complex" ALE environment

In Part 3, we address a more complex single-agent Atari environment,
**MsPacmanNoFrameskip-v4**, using the **ALE Gymnasium** interface.

Multiple deep reinforcement learning algorithms (**PPO, DQN, and A2C**) are
trained and compared using **Stable-Baselines3**. Standard Atari preprocessing
and frame stacking are applied, and vectorized environments are used to improve
training efficiency.

Models are trained with carefully selected hyperparameters, evaluated periodically,
and compared using learning curves, average episode rewards, and recorded gameplay
videos. The results are analyzed to assess training stability, sample efficiency,
and final performance, and to justify the selection of the best-performing model
for this environment.

---

## Reproducibility

Each part of the project includes:
- Well-documented source code
- Saved models 
- Visualization of learning curves and agent behavior
