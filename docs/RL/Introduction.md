# Reinforcement Learning Notes

## Learning Through Interaction

- Learning by interacting with the environment is fundamental to intelligence.

- Understanding cause and effect, consequences of actions, and goal-directed behavior is essential.

- Interaction-based learning forms the foundation of many theories of learning and artificial intelligence.

## Reinforcement Learning (RL)

- RL is focused on goal-directed learning from interaction, differing from other machine learning approaches.

- It involves **learning what to do**—how to map situations to actions—to **maximize a numerical reward signal**.

- **Trial-and-error search** and **delayed reward** are key distinguishing features of RL.

## Formalizing Reinforcement Learning

- RL problems are framed using **dynamical systems theory**.

- A **learning agent** must:

	- Sense the state of its environment.

	- Take actions that affect the environment.

	- Have goals related to the environment's state.

- **Markov Decision Processes (MDPs)**  capture these three essential aspects: **sensation**, **action**, and **goal**.

# Comparison with Supervised and Unsupervised Learning

**Supervised Learning**

- Involves learning from a labeled dataset provided by an external supervisor.

- The goal is to generalize from labeled examples to new, unseen situations.

- **Limitation**: Supervised learning is impractical in interactive problems where labeled examples are scarce or unavailable.

**Unsupervised Learning**

- Focuses on discovering hidden structures in unlabeled data.

- RL is not unsupervised learning because it aims to **maximize a reward signal**, not just uncover patterns.

- Although structure discovery can be useful in RL, it does not directly address the goal of reward maximization.

# RL as a Distinct Machine Learning Paradigm

- RL stands alongside **supervised learning** and **unsupervised learning** as a third paradigm.

- Unlike supervised learning, RL does not require labeled examples.

- Unlike unsupervised learning, RL focuses on optimizing a **reward signal** rather than just finding patterns.

- In **uncharted territories**, RL allows agents to learn **from their own experience** rather than pre-existing data.

# Exploration vs. Exploitation

One of the key challenges in reinforcement learning, which does not arise in other forms of learning, is the **trade-off between exploration and exploitation.**

- **Exploration**: The agent tries new actions to discover their effects.

- **Exploitation**: The agent uses known actions that yield high rewards.

In **supervised and unsupervised learning**, this trade-off does not arise in the same way.

# Example

Imagine a **multi-armed bandit** scenario:

- You are at a casino with multiple slot machines.

- Each machine has an unknown payout probability.

- You need to decide whether to **try a new machine (exploration) or stick to a machine that has given high rewards (exploitation).**

- The goal is to **maximize total reward over time.**

Mathematically, the epsilon-greedy algorithm balances exploration and exploitation:

\[
\pi(a | s) =
\begin{cases} 
1 - \epsilon + \frac{\epsilon}{|\mathcal{A}|}, & \text{if } a = \arg\max_{a'} Q(s, a') \\
\frac{\epsilon}{|\mathcal{A}|}, & \text{otherwise}
\end{cases}
\]

where:
- **\( \pi(a | s) \)** is the probability of selecting action **\( a \)** in state **\( s \)**.
- **\( \epsilon \)** is the exploration probability **(typically a small value like 0.1)**.
- **\( Q(s, a) \)** is the estimated value of action **\( a \) in state \( s \)**.
- **\( |\mathcal{A}| \)** is the total number of possible actions.

### Explanation:
- With probability **\( 1 - \epsilon \)**, the agent **exploits** the action with the highest Q-value.
- With probability **\( \epsilon \)**, the agent **explores** by selecting a random action.

This ensures that the agent does not get stuck in local optima and continues exploring better strategies.

