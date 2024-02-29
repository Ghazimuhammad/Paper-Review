# Massive MIMO Power Allocation Using Deep Reinforcement Learning

## About

| Item | Information | 
| -------- | -------- | 
|Paper Link|https://ieeexplore.ieee.org/document/10299873|
|Authors|Huynh Vu Hoang Phuc, Ha Hoang Kha|
|Date of Publication|19-20 October 2023|
|Total Pages|6|
|Keywords|Massive MIMO, power allocation, spectral efficiency, deep reinforcement learning|

This paper studies the power allocation strategy in massive multiple-input multiple-output (MIMO) wireless networks to maximize the sum spectral efficiency (SE) in the
downlink transmission. 

## Introduction
Massive MIMO (Multiple-Input Multiple-Output) is a technology that integrates a large number of antennas at the base station (BS) to serve multiple user equipments (UEs)
simultaneously. In massive MIMO, power allocation strategies are crucial to affect the SE. Conventionally, to obtain suitable power allocation strategies that produce the optimal SE for massive MIMO networks to meet certain criteria, optimization methods with high computational complexity such as geometric programming (GP) must be deployed. 

This paper explores the possibility of incorporating an actor-critic based DRL algorithm into solving the SE maximization problem in massive MIMO. Traditional nonlinear optimization methods, known for their high computational complexity, are replaced with a DRL approach utilizing a Twin-Delayed Deep Deterministic Policy Gradient (TD3) framework. This approach aims at maximizing the expected cumulative long-term reward in terms of SE. Numerical results demonstrate the effectiveness of the DRL framework in achieving high SE compared to traditional optimization algorithms, showcasing the potential of DRL in simplifying and optimizing power allocation in massive MIMO networks.

## Massive MIMO and Power Allocation 
* massive MIMO network with multiple cells, each consisting of a base station (BS) with M antennas and K single-antenna user equipment (UE).
* The network operates using a 3-phase time-division duplex (TDD) protocol, including channel estimation, uplink (UL) and downlink (DL) transmission.
* Minimum mean squared error (MMSE) estimator is used for channel estimation using reusable pilot sequences.
* During UL transmission, a BS can filter out interference and noise by designing a linear filter.
* In DL transmission, the SE of the channel between a BS and UE is given by equation
![image](https://hackmd.io/_uploads/SJFg9ci3p.png)
* The total achievable SE of a massive MIMO network is evaluated through an optimization problem with power allocation constraints.
![image](https://hackmd.io/_uploads/HywHi9snT.png)

## Power Allocation with Deep Reinforcement Learning
![image](https://hackmd.io/_uploads/S1pQnconp.png)
* The power allocation problem in a massive MIMO system can be modeled as a DRL model with the BS as the learning agent.
* In DRL, the agent interacts with the environment and applies actions to change the state. The agent's objective is to maximize the total reward received until reaching the termination state.
* Actor-critic is a common algorithm used in DRL for continuous action and state spaces, where an actor produces actions based on the environment state and a critic computes the action-value.
* The actor and critic networks have a dependency relationship, with the critic estimating the value and the actor updating its weights based on the gradient of the policy.
* The update rule in the DRL model has a flaw where the gain function of the actor and the loss function of the critic change at the same pace, leading to unstable solutions. To mitigate this, delayed and weighted copies of the actor and critic are introduced as target networks, which are updated at a slower pace.
* Another drawback is the use of the max() function, which can cause overestimation bias. To address this, two target critic networks are used, and the smaller output is chosen for the update target. To prevent overfitting, a regularization factor is added to the output of the target actor network.

## Simulation Results
* The TD3 DRL model is evaluated and compared with GP in terms of average total DL SE for wrapped-around massive MIMO networks.
* The TD3 DRL algorithm achieves an average total achievable DL SE of 56.27 bps/Hz, which is 93.66% of the GP approach.
* The cumulative distribution functions (CDFs) of total DL SE achieved by both methods are presented in Fig.2

![image](https://github.com/Ghazimuhammad/Paper-Review/blob/main/images/DRL%20result.png)

* The average achievable sum DL SE in the massive MIMO network increases with the number of antennas, and the results obtained by TD3 DRL are comparable to those from the GP.
* The achievable sum SE increases significantly when the transmit power budgets increase from 100 mW to 150 mW, but the increase is negligible when the transmit power budgets increase from 200 mW to 20 mW.

![image](https://github.com/Ghazimuhammad/Paper-Review/blob/main/images/DRL%20result2.png)

## Conclusion


