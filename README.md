# Banana-collector
Deep reinforcement learning agent that catches yellow bananas in unity environment. This project is the first graded project for the Deep Reinforcement Learning Nanodegree on Udacity.

An agent is trained to navigate and locate yellow bananas on a Unity environment. The agent is rewarded +1 when it collects a yellow banana and -1 when it collects a blue banana. 

The environment consists of a 37 dimension state space, and 4 discrete action space. The task is episodic, meaning there is an end, in this case of 100 steps and trying to achieve a score of at least +13 over 100 episodes.

I implemented a double DQN agent.


[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"

![Trained Agent][image1]

### Steps to get this thing going
1. Create a new environment with python version 3.6.x `conda create -n bananas python=3.6`
2. Activate your environment `conda activate bananas`
3. Install mlagents `pip install mlagents==0.4.0`
4. Install pytorch, get your command from https://pytorch.org/get-started/locally/ in my case it is `conda install pytorch torchvision cudatoolkit=10.1 -c pytorch`
5. Install jupyter lab (it looks good) `pip install jupyterlab`
6. Clone this repository `git clone https://github.com/juanluislopez24/banana-collector.git`
7. Download the environment from one of the links below.  You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)

8. Uncompress the zip file you desired folder

9. Open jupyter lab with `jupyter lab` and open the Navigation.ipynb file
10. Change the path for your unity environment on the cell that has `env = UnityEnvironment(file_name="./envs/Banana_Windows_x86_64/Banana.exe")`
11. Run all the cells and train a new agent, or go down until the section of "Run the trained agent" and run all the remaining cells.


Have fun and thanks for passing through here!
