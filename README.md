# reinforcement-learning-process-journal
## Overview
This repository documents my work studying reinforcement learning, as part of Andover's CSC600 in winter 2020-2021.

I draw from Sutton and Barto's [*Reinforcement Learning: An Introduction*](http://incompleteideas.net/book/RLbook2018.pdf), David Silver's [UCL Reinforcement Learning Course](https://www.davidsilver.uk/teaching/), Denny Britz's [repository](https://github.com/dennybritz/reinforcement-learning) of accompanying exercises and implementations, and Miguel Morales' [*Grokking Deep Reinforcement Learning*](https://livebook.manning.com/book/grokking-deep-reinforcement-learning/)

## Process Journal
### Introduction to RL
*What is RL–what questions is it trying to solve, and what approaches/components does it employ to do so?*

Materials:
- Sutton and Barto Ch. 1: a non-technical overview of RL
- Silver [lecture 1](https://www.youtube.com/watch?v=2pWv7GOvuf0): similar to Sutton and Barto but with slightly more technical detail
- Morales Ch. 1-2: a first pass over the big ideas of RL and its mathematical foundations, which acts as a helpful primer for the more rigorous definitions from Sutton and Barto and Silver later on

Takeaways:
- Definitions of **agent-environment interaction, action, reward, history, state, policy, model, and value functions**
- For more detail, see these [lecture notes](./notes/silver_notes/lecture1.md)
### Overview of AI Economist
*What RL topics are most central for understanding AI Economist specifically?*

Materials:
- [AI Economist paper](https://arxiv.org/abs/2004.13332): on a first pass, an opportunity to understand the model with a few basic RL definitions under my belt

Takeaways:
- AI Economist operates within a **multi-agent RL simulation**
- Agents are trained using **model-free** RL and an part of a **partially-observable Markov decision process**
- The simulation allows researchers to avoid making general economic assumptions and instead model human-like behavior via the RL agents
### Exploration of AI Economist Codebase (Foundation) and OpenAI Gym
*How does Foundation enable users to run multi-agent economic simulations? How can I use code to actually implement and run RL agents using Foundation or Gym?*

Materials:
- AI Economist [tutorials](https://github.com/salesforce/ai-economist/tree/master/tutorials) (basic, advanced, and optimal taxation): an introduction to how Foundation works and how it can be modified or extended to examine different economic problems
- [OpenAI Gym tutorial](https://gym.openai.com/docs/): an introduction to environment, observation, reward, done, and info **variables** as well as action and observation spaces

Takeaways:
- Foundation employs a high-level gym-style API, which I should become familiar with
- How to run, sample, and visualize an episode using Foundation
- Foundation's structure and use of Scenario, World, Entities, Agents, and Components to create simulations
### Markov Decision Processes: Defining the RL Problem
*What is a MDP? What is the rigorous formulation of the RL problem, and how does it involve concepts like actions, states, rewards, policies, returns, and value functions?*

Materials:
- Sutton and Barto Ch. 3: reading, annotating, and doing the exercises from this chapter will yield a solid mathematical understanding of the RL problem
- Silver [lecture 2](https://www.youtube.com/watch?v=lfHX2hHRMVQ): watching the lecture clarifies the topics covered by Sutton and Barto

Takeaways:
- An MDP is a tuple of a set of states, a set of actions, a state transition probability matrix (determines dynamics of the environment), a reward function, an a discount factor
- Definitions of return (expected future reward), state-value (v) and action-value (q) functions, and optimal state-value and action-value functions
- Bellman equations recursively define the value of states in terms of the value of other states, and they come in expectation and optimality flavors
- For more detail, see these [lecture notes](./notes/silver_notes/lecture2.md)
### Policy and Value Iteration using Dynamic Programming
*Given complete knowledge of an MDP, how can one approach the planning problem?*

Materials: 
- David Silver's [lecture 3](https://www.youtube.com/watch?v=Nd1-UUMVfz4&ab_channel=DeepMind): an overview of DP and its relevance to the RL planning problem
- Denny Britz' [section 3](https://github.com/dennybritz/reinforcement-learning/tree/master/DP) exercises: a chance to implement the algorithms discussed in Silver's lecture

Takeaways:
- DP is a general approach to solve problems that can be decomposed into subproblems. Given a full definition of a MDP and a certain policy, DP can predict the corresponding value function. From an MDP, DP can also determine the optimal value function (and thus the optimal policy).
- Policy evaluation and policy iteration or value iteration enable you to identify optimal policies
- For more detail, see these [lecture notes](./notes/silver_notes/lecture3.md)
