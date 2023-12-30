# Multi-Armed Bandit Simulation

## Overview

This script simulates a multi-armed bandit problem using an epsilon-greedy strategy for the agent. The multi-armed bandit problem is a classic reinforcement learning problem that illustrates the exploration-exploitation tradeoff. An agent is faced with several options (arms), each providing a stochastic reward, and it aims to maximize its total reward over time by learning the best arms to pull.

## How It Works

### Environment

- **Arms**: The environment consists of a set number of arms (slot machines), each with a fixed but unknown probability of providing a reward when pulled.

### Agent

- **Epsilon-Greedy Strategy**: The agent follows an epsilon-greedy strategy, where it explores (pulls a random arm) with a probability `eps` and exploits (pulls the best-known arm) with probability `1-eps`.
- **Action-Value Estimation**: The agent maintains an estimate of the value (expected reward) of each action and updates these estimates based on the observed rewards.

### Simulation Flow

1. **Initialize**: The environment and agent are initialized with the given probabilities and parameters.
2. **Run Experiments**: The agent repeatedly interacts with the environment over several episodes, choosing actions and receiving rewards.
3. **Update**: After each action, the agent updates its action-value estimates based on the received reward.
4. **Repeat**: Steps 2 and 3 are repeated for a specified number of steps and experiments.

## Usage

1. **Set Parameters**: Define the probabilities of success for each arm, the number of experiments, steps per experiment, and the exploration fraction (eps).
2. **Run**: Execute the script to perform the multi-armed bandit experiments.
3. **Results**: Observe the average rewards and action selection percentages in the output plots.

## Output

- **Average Reward Plot**: Shows how the average reward received by the agent evolves over time.
- **Action Selection Percentage Plot**: Shows the percentage of times each arm was selected by the agent over time.

## Key Variables

- `probs`: A list of success probabilities for each arm.
- `N_experiments`: The number of experiments to perform.
- `N_steps`: The number of steps (episodes) in each experiment.
- `eps`: The probability of choosing an action randomly (exploration rate).
- `save_fig`: A boolean to decide whether to save plots as images.

## Conclusion

This script is an implementation of a simple epsilon-greedy agent solving the multi-armed bandit problem. It provides foundational insights into how agents can learn and make decisions in uncertain environments, balancing the need to explore new options and exploit known ones.

