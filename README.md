# FrozenLake Q-Learning

This project implements tabular Q-learning to train an agent to navigate the FrozenLake 8×8 environment using Gymnasium.

## Environment

The agent must navigate from the starting position to the goal while avoiding holes. The environment contains 64 discrete states and 4 possible actions: left, down, right, and up.

The environment uses stochastic transitions (is_slippery=True), making it more challenging for the agent to reach the goal.

## Q-Learning Implementation

The agent uses a Q-table initialized with zeros and an epsilon-greedy policy for action selection. The Q-values are updated after each action using the learning rate and discount factor.

## Hyperparameter Experiments

Three experiments were conducted:

Learning rate: 0.1, 0.5, 0.9

Discount factor: 0.5, 0.9, 0.99

Epsilon decay: 0.999, 0.9995, 0.9999

Each configuration was trained for 20,000 episodes.

## Best Agent

The selected hyperparameters were:

Learning rate: 0.1

Discount factor: 0.99

Epsilon decay: 0.999

The final agent was evaluated over 100 episodes without exploration.

Evaluation results:

Mean reward: 0.50

Success rate: 50%

Average steps per episode: 66.63

## Requirements

Python 3.11

Gymnasium

NumPy

Matplotlib

Jupyter Notebook

## Running the Project

Install the required libraries:

pip install "gymnasium[toy-text]" numpy matplotlib notebook ipykernel

Open frozenlake_qlearning.ipynb in Jupyter Notebook or VS Code.

Run the notebook cells in order to train and evaluate the agent.