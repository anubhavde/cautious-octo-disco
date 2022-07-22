#### cautious-octo-disco

# **OpenAI CartPole Solution using Actor Critic method**

Performed the [tutorial](https://www.tensorflow.org/tutorials/reinforcement_learning/actor_critic) to implement the Actor-Critic using TensorFlow to train an agent on the Open AI Gym CartPole-V0 environment.

**Actor-Critic methods**

Actor-Critic learning methods reflect the policy function independently of the value function using temporal difference (TD) learning techniques.

Based on the provided state, a policy function (or policy) produces a probability distribution across the possible actions the agent may take. The expected return for an agent starting at a specific state and behaving consistently with a specific policy is determined by a value function.

The policy is referred to as the actor in the Actor-Critic technique, proposing a set of feasible actions given a state, and the estimated value function is referred to as the critic, assessing the actor's actions in light of the provided policy.

**CartPole-v0**

In the CartPole-v0 environment, a pole is attached to a cart moving along a frictionless track. The pole starts upright and the goal of the agent is to prevent it from falling over by applying a force of -1 or +1 to the cart. A reward of +1 is given for every time step the pole remains upright. An episode ends when 
- The pole is more than 15 degrees from vertical.
- The cart moves more than 2.4 units from the center.

The problem is considered "solved" when the average total reward for the episode reaches 195 over 100 consecutive trials.

### **SETUP**

Run the following commands in the jupyter notebook:
```python
pip install gym[classic_control]
pip install pyglet

```
Then install the additional packages for visualization:
```python
sudo apt-get install -y xvfb python-opengl > /dev/null 2>&1
pip install pyvirtualdisplay > /dev/null 2>&1
pip install git+https://github.com/tensorflow/docs > /dev/null 2>&1
```

### **VISUALIZATION**

After training, for understanding and research purposes, visualize how the model performs in the environment by creating a GIF animation of one episode run of the model. 
