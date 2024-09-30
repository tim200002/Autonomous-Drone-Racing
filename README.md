# Autonomous-Drone-Racing
This repository showcases the work I completed as part of the Autonomous Drone Racing Project course at the Technical University of Munich (TUM). The primary objective was to design a control system that enables an autonomous drone to navigate a racing track as quickly as possible. A key challenge in our setting was the uncertainty in the track layout, with gate positions only approximately known, requiring the drone to replan dynamically as new information became available.

As the sole student working independently, I successfully implemented two control strategies: a classical optimization approach, which achieved the highest robustness among all teams, and a reinforcement learning approach, which delivered the fastest race time.

You can access the [report](todo) and [presentation](todo) through these links. The code for the optimization approach is available in [this GitHub repository](todo), and the code for the reinforcement learning agent can be found [here](todo).

## Abstract
Autonomous drone racing has long been researched as a benchmark task for testing control approaches at their limits. While most work focuses on the disturbance-free case, robustness to disturbances in drone dynamics and environmental conditions is important for the real-world deployment of such algorithms. This work presents two approaches that enable autonomous drone racing under disturbances. The first approach is built around subsequent path planning and trajectory generation and demonstrates how, by focusing on computationally efficient implementations, within-flight re-planning is possible and enables high robustness to shifting gates.  The second reinforcement learning-based (RL) approach demonstrates that RL can successfully adapt to the domain shifts introduced by disturbances, unifying best-in-class flight times with good robustness levels.

## Reinforcement Learning-Based Drone Racing
I trained a reinforcement learning agent to safely navigate the disturbed racing course more than halving the given baseline time from 12.47s to 5.17s while still achieving a high success rate of >70%. The learnings I did to achieve at this performance are summarized in [my report]()

**Watch a video of the drone flying in simulation**

https://github.com/user-attachments/assets/fc6d0d36-8d82-4e43-85f6-6a8dddc8add3



## Optimization-Based Drone Racing
I implemented a traditional optimization approach, consisting of path planning and trajectory generation that, while not as fast as RL, achieved very high success rates. The key challenge in this approach was that path-planning and trajectory generation is typically compute intensive. We, however, required real-time re-planning capabilities and thefore I implemented all code in multi-threaded C++. All information is available in [my report](). I was furthermore capable of transferring the control approach from simulation to a real drone.

**Watch a video of the drone flying in simulation**


https://github.com/user-attachments/assets/1220c219-2222-4eef-9d95-2a2dc81b3796



**Watch a video of the drone flying in the real world**

https://github.com/user-attachments/assets/c2cd7d34-42df-4cda-9f03-17945144ea69

