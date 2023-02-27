# Accelerating Spatiotemporal Neural Process Simulator with Deep Reinforcement Learning


# Abstract

This paper proposes a deep reinforcement learning approach to improve the efficiency of COVID-19 pandemic simulation. The pandemic simulation is modeled using the spatiotemporal neural network (STNP) and the Neural Process (NP) family. To enhance the computational efficiency, the STNP model employs Bayesian active learning to query the simulator for data. However, the brute-force search approach for exploring the best parameter set is inefficient. Our proposed framework replaces the acquisition function with a DeepQ reinforcement learning network, where the reward of a parameter set is estimated with Q-values.In this quarter 2 project, we aim to implement the proposed framework and examine its performance with different reward functions.

# Introduction

Accurate COVID-19 simulation is crucial to evaluate the impact of external factors. In this paper, we propose a deep reinforcement learning approach to improve the efficiency of COVID-19 pandemic simulation. The pandemic simulation, a crucial tool for evaluating the impact of policy measures, is modeled using the spatiotemporal neural network (STNP) and the Neural Process (NP) family. To enhance the computational efficiency, the STNP model employs Bayesian active learning to query the simulator for data. However, the brute-force search approach for exploring the best parameter set is inefficient. Our proposed framework replaces the acquisition function with a DeepQ reinforcement learning network, where the reward of a parameter set is estimated with Q-values. The model outputs the Q-values of choosing each parameter set, allowing the model to efficiently explore the parameter space and identify the parameter set with the best reward. In this quarter 2 project, we aim to implement the proposed framework and examine its performance with different reward functions.

# Methodology

The DQN is trained using reinforcement learning, wherein the neural networks minimize loss between the predicted Q-values and the true Q-value. 

Instead of the brute force method finding the maximum reward, the DQN uses experience replay to more efficiently calculate the reward

Our reward function will be computed with the STNP reward function, namely the acquisition function of Latent Information Gain (LIG). Given the state information and parameter information, the model will ideally learn the mapping function of the acquisition function.
