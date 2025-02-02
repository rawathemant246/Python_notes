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