# Review Paper

## 1. Reinforcement learning approach for Advanced Sleep Modes management in 5G networks

| Item | Information | 
| -------- | -------- | 
|Paper Link|https://ieeexplore.ieee.org/document/8690555|
|Authors|Fatma Ezzahra Salema, Zwi Altmana, Azeddine Gatia, Tijani Chahedb, Eitan Altmanc|
|Date of Publication|27 - 30 August 2018|
|Total Pages|5|
|Keywords|Advanced Sleep Modes, Energy Consumption, Q-learning.|

### 1.1 Summary
This paper aims to optimize Advanced Sleep Modes (ASM) with Q-learning approach in order to find the optimal duration for each SM level. This paper focus on distributed architecture where each BS uses solely its local information in order to learn the energy-saving policy. 

| Sleep level | Deactivation duration | Minimum sleep duration | Activation duration |
|-------------|-----------------------|------------------------|---------------------|
| SM1         | 35.5 µs               | 71 µs                  | 35.5 µs             |
| SM2         | 0.5 ms                | 1 ms                   | 0.5 ms              |
| SM3         | 5 ms                  | 10 ms                  | 5 ms                |
| SM4         | 0.5 s                 | 1 s                    | 0.5 s               |

This paper proposes the use of Q-Learning model, a type of model free-learning reinforcement learning, for find optimal action-selection policy for any given (finite) Markov decision process (MDP). The Q-Learning model doesn't require a model of environment, so it's suitable for problem that may have complex environment model or unknown environtment model.

The proposes strategy aims to manage energy savings in base stations (BS) without inducing latency. Upon a user's departure, if the BS is idle, it is switched to the most energy-saving sleep mode (SM3). The system must determine how many times to repeat SM3 before transitioning to a less deep sleep mode (SM2), and subsequently, how many times to repeat SM2 before moving to SM1. Finally, it must decide the duration in SM1 before the BS fully wakes up. If minimizing delay is crucial, the BS will wake up sooner, potentially reducing energy savings. Conversely, if energy conservation (EC) is the sole concern, the BS will remain in deeper sleep modes for as long as possible.





### Data, Pros, and Cons
<div style="background-color: #ADD8E6; padding: 10px;">

## 1.2 Pros and Cons

**PROS**
* Energy Savings: The management solution proposed using Q-learning can achieve substantial energy savings, up to 57% with stringent delay constraints and nearly 90% under more relaxed delay conditions. This contributes to reduced operational costs and less environmental impact.

* Decentralization: Each base station operates using solely its local information to learn the energy-saving policy, which simplifies the complexity of system-wide updates and reduces dependencies on centralized control.

* No Prior Model Needed: The Q-learning algorithm used does not require an explicit model of the environment, which is beneficial in a dynamic real-world scenario where transition probabilities and other parameters may not be readily known.
    
**CONS**
* Increased Latency: Implementing ASMs can lead to increased latency because of the time it takes for base stations to reactivate from sleep modes. This can be problematic for delay-sensitive applications, requiring careful management and policy setting to avoid service degradation.

* Trade-offs Requirement: There is a need to constantly balance between achieving lower energy consumption and maintaining acceptable levels of service delay. Finding the optimal balance requires continuous adjustments and may not always meet all operational expectations simultaneously.


