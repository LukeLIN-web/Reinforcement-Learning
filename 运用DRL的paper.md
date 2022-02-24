利用DRL的一些paper



SINET: Enabling Scalable Network Routing with Deep Reinforcement Learning on Partial Nodes



NetAI@SIGCOMM 2019 workshop

1. **Cracking Open the Black Box: What Observations Can Tell Us About Reinforcement Learning Agents**
2.  **Runtime Verification of P4 Switches with Reinforcement Learning.**



SIGCOMM 2018

**AuTO: scaling deep reinforcement learning for datacenter-scale automatic traffic optimization**

chenkai老师的文章,  也是两级, 一级DRL, 进行Traffic optimizations.

解决的问题:  一开始要验证有效性, 但是太多了不太行, 让DRL scalable.  利用多阈值. 

We started by verifying DRL’s effectiveness in TO. We implemented a flow-level centralized TO system with a basic DRL algorithm, policy gradient [55]. However, in our experiments (§2.2), even this simple algorithm running on current machine learning software frameworks2 and advanced hardware (GPU) cannot handle traffic optimization tasks at the scale of production datacenters (>10^5 servers). The crux is the computation time (∼100ms): short flows (which constitute the majority of the flows) are gone before the DRL decisions come back, rendering most decisions useless. 决策速度太慢

他是怎么两级的? 一级DRL 来优化 阈值.  ,确定优先级和速度. 

The CS is composed of two DRL agents (RLA): short flowRLA (sRLA) is for optimizing thresholds for MLFQ, and long flow RLA (lRLA) is for determining rates, routes, and priorities for long flows. sRLA attempts to solve a FCT minimization problem, and we develop a Deep Deterministic Policy Gradient algorithm for this purpose. For lRLA, we use a PG algorithm (§2.2) to generate actions for the long flows. In the next section, we describe the two DRL problems and solutions.



**IFS-RL: An Intelligent Forwarding Strategy Based on Reinforcement Learning in Named-Data Networking**



ijcai19  hybird actor-critic reinforcement learning in parameterized action space.

