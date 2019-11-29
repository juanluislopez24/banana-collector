# Report
### Learning Algorithm
I implemented double DQN. I took the base from the lunar Lander agent, and adapted it for this project. I implemented double DQN since it consists of a small change to the DQN learning function. 

The hyperparameters I chose are:
- BUFFER_SIZE = 100000
- BATCH_SIZE = 32
- GAMMA = 0.99
- TAU = 0.001
- LR = 0.00025
- UPDATE_EVERY = 4
- E = 0.1

I trained the agent for 1000 episodes, reaching an average score of 16.91 through 100 episodes. This agent performed better, more consistently through time, than the simple DQN algorithm, probably because the advantages of not overstimating values from the double DQN.  


### Plot of Rewards 
[image1]: rewards.PNG "rewards"
![Rewards][image1]

As you can see, the agent started getting consistent +13 score since episode 450. 

### Ideas for Future Work
I tried implementing Prioritized experience replay, and it worked pretty well up until the end. It learned a little faster than a simple DQN, but became unstable towards the end. Thats when I learned that bias can really affect you, since the learning on prioritized episodes only. Thats when I realized I was missing the piece of implementing importance sampling weights, but couldnt achieve the agent to learn. I will finish that. After that I will be able to train the agent with double DQN and prioritized experience replay.

Another area of improvement is to use a rainbow DQN, by adding the dueling DQN networks. This way Q values and action-values(advantage values) are computed separately. This allows to learn which states are good, without exploring every action space on each state. 