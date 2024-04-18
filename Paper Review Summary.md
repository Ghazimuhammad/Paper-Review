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

### Pros and Cons
<div style="background-color: #ADD8E6; padding: 10px;">

## 1.2 Pros and Cons

**PROS**
* Energy Savings: The management solution proposed using Q-learning can achieve substantial energy savings, up to 57% with stringent delay constraints and nearly 90% under more relaxed delay conditions. This contributes to reduced operational costs and less environmental impact.

* Decentralization: Each base station operates using solely its local information to learn the energy-saving policy, which simplifies the complexity of system-wide updates and reduces dependencies on centralized control.

* No Prior Model Needed: The Q-learning algorithm used does not require an explicit model of the environment, which is beneficial in a dynamic real-world scenario where transition probabilities and other parameters may not be readily known.
    
**CONS**
* Increased Latency: Implementing ASMs can lead to increased latency because of the time it takes for base stations to reactivate from sleep modes. This can be problematic for delay-sensitive applications, requiring careful management and policy setting to avoid service degradation.

* Trade-offs Requirement: There is a need to constantly balance between achieving lower energy consumption and maintaining acceptable levels of service delay. Finding the optimal balance requires continuous adjustments and may not always meet all operational expectations simultaneously.

</div>
    
## 2. Advanced Sleep Modes in 5G Multiple Base Stations using Non-cooperative Multi-Agent Reinforcement Learning

| Item | Information | 
| -------- | -------- | 
|Paper Link|https://ieeexplore.ieee.org/document/10437599/|
|Authors|Amal Abdel Razzac, Tijani Chahed|
|Date of Publication|04-08 December 2023|
|Total Pages|6|
|Keywords|multiple base stations, Advanced Sleep Modes, Multi-Agent Reinforcement Learning, energy saving versus delay performance trade-off|

This paper aims to to explore the implementation of advanced sleep modes (ASM) in 5G base stations to improve energy efficiency without significantly impacting service delay. The study specifically investigates the trade-off between energy savings and service delay by considering the effects of inter-cell interference on decision-making processes related to waking up the base stations upon traffic arrival or continuing to stay in sleep mode.


The conclusion of the paper highlights that advanced sleep modes (ASM) in 5G base stations can significantly save energy while managing delays in service. Using a special learning method, each base station independently adjusts when to wake up or stay asleep based on traffic and interference, balancing energy savings with service quality. The research shows that these strategies can be adapted based on how busy the network is and the importance of saving power versus reducing delays. Future studies will look into how base stations can work together to optimize both energy efficiency and service delays across the network.

### Pros and Cons
<div style="background-color: #ADD8E6; padding: 10px;">

## 2.2 Pros and Cons

**PROS**
* Flexibility in Service Quality Management: The system can balance energy savings with acceptable levels of service delay, providing flexibility in how performance trade-offs are managed depending on current network demands.
* Autonomy: Each base station operates independently to optimize its policies, which can be beneficial in complex network environments where centralized control might be inefficient.
    
**CONS**
* Complexity in Implementation: The non-cooperative multi-agent learning model adds complexity to the system's implementation and requires sophisticated algorithms that can handle dynamic and uncertain environments.
    
* Potential for Suboptimal Performance: Since each base station makes decisions independently without cooperation, there is a risk of suboptimal performance due to a lack of coordination, potentially leading to increased interference or delays under certain conditions.

</div>

