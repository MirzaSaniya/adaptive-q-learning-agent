# Adaptive Q-Learning Agent

A from-scratch reinforcement-learning project where an agent learns how to navigate a small environment using **Q-learning** instead of being given an optimal policy.

## Use case

The same pattern appears in adaptive control, robotics, recommendation strategies, and resource management: the agent observes a state, takes an action, receives a reward, and improves its behavior from experience.

## Environment

The demo uses a compact GridWorld with:

- start state
- goal state
- blocked cells
- step costs
- terminal reward

## Algorithm

Q-learning updates the action-value estimate using the observed reward and the best estimated future value:

`Q(s,a) <- Q(s,a) + alpha * (r + gamma * max Q(s',a') - Q(s,a))`

The project includes epsilon-greedy exploration and records episode rewards for analysis.

## Run

```bash
python examples/demo.py
```

## Tests

```bash
pytest -q
```

## Experiments to showcase

- epsilon decay vs. fixed exploration
- learning curves across random seeds
- impact of discount factor
- greedy policy after training

## CS221 connection

Inspired by reinforcement-learning concepts commonly covered in CS221. The environment, implementation, experiments, and presentation are independently developed.

## GitHub metadata

**Repository name:** `adaptive-q-learning-agent`

**Description:** A reinforcement-learning agent that learns optimal actions through Q-learning and exploration-exploitation tradeoffs.

**Topics:** `artificial-intelligence` `reinforcement-learning` `q-learning` `machine-learning` `exploration-exploitation` `python` `gridworld` `cs221`
