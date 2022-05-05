# ITI110 - Deep Learning Project

## **Description**
- Reinforcement learning Deep Q-Network using Carla simulator.  
- Credits to https://github.com/EmanueleBenedettini/DQN-Autonomous-Vehicle-on-CARLA
- Deep Q-Network:
    - Neural network to approximate Q-value function. State is given as the input and the Q-value of all possible actions is generated as the output. past experience is stored in memory, subsequently the next action is determined by the maximum output of the Q-network, then update Q-values as derived from the Bellman equation and the network updates its gradient using backpropagation to reach convergence.
    - 1st technique: Experience replay stores agent's experiences and makes mini-batches to update neural networks. For our experiments, we put the last 100,000 video frames into a video buffer and randomly sample a mini-batch of samples from this to train the deep network, making the data more independent of each other
    - 2nd technique: Target network technique two deep networks are created where one retrieves Q values and the other includes all updates in the training, and after C iterations the first deep network is synchronized with the second.
    - 3rd technique: Clipping rewards
    - 4th technique: Skipping frames, DQN calculates Q values every n frames, reduce computational costs
- 6 experimental runs with changes to reward function, CNN complexity, epsilon, epsilon minimum, image dimensions
- Observations:
    - Arbitrary large rewards caused Q-values and loss explosion. Future rewards kept at -1, +1
    - Use simpler CNN with fewer learnable parameters
    - When epsilon set to 0, car agent tends to perform only one action. For future runs, use high epsilon at beginning for exploration
    - Exploration for episodes at the tail-end of the run is encouraged especially when the environment is large and numerous actors are involved
    - 84 X 84 image dimension produced more favourable results than 168 X 168. Leading back to above point that CNN with fewer trainable parameters favoured, as in context of calculating loss against changing ground-truths in DQN. 
- Demo of result:
    - https://youtu.be/G1Y9H1iqY8c
    - https://youtu.be/tDV37bbLN9w
    - https://youtu.be/L5CRrl758Yc
    
## **Report excerpts**
[![Capture.png](https://i.postimg.cc/LsSNYSpL/Capture.png)](https://postimg.cc/rDhS3vzw)

[![Capture.png](https://i.postimg.cc/VkQFpw5p/Capture.png)](https://postimg.cc/7f97Jp3n)

[![Capture100.png](https://i.postimg.cc/HW72WjGj/Capture100.png)](https://postimg.cc/14s6Jm3Z)

[![Capture.png](https://i.postimg.cc/Dzd6TMR6/Capture.png)](https://postimg.cc/5HyL5n4Q)

[![Capture2.png](https://i.postimg.cc/fbKcF00g/Capture2.png)](https://postimg.cc/JysHH0xb)

[![Capture3.png](https://i.postimg.cc/GtBvH7gZ/Capture3.png)](https://postimg.cc/K321WN2N)

[![Capture4.png](https://i.postimg.cc/ZnyyT9Cm/Capture4.png)](https://postimg.cc/2Lr5GSQ9)



