Neural Combinatorial Optimization With Reinforcement Learning
=============================================================
#### Irwan Bello, Hieu Pham, Quoc V. Le, Mohammad Norouzi, Samy Bengio
##### ICLR 2017: [pdf](https://arxiv.org/pdf/1611.09940.pdf)

![img](https://upload.wikimedia.org/wikipedia/commons/2/2b/Bruteforce.gif)
- Solution to a symmetric TSP with 7 cities using brute force search. Note: Number of permutations: (7-1)!/2 = 360!

#### Resources
- [Lecture 14 | Deep Reinforcement Learning](https://youtu.be/lvoHnicueoE)
Stanford University School of Engineering
- [Demystifying Deep Reinforcement
Learning](https://www.intel.ai/demystifying-deep-reinforcement-learning/) Tambet Matiisen
- [Reinforcement Learning: An
Introduction](http://incompleteideas.net/book/the-book-2nd.html) Richard S.
Sutton and Andrew G. Barto
- [Deep Reinforcement Learning: Pong from
Pixels](http://karpathy.github.io/2016/05/31/rl/) Andrej Karpathy

#### Markov Decision Process
A Markov decision process relies on the Markov assumption, that the probability
of the next state s[i+1] depends only on current state s[i] and action a[i],
but not on preceding states or actions.

#### Action, Reward, State, and Policy
- [Google DeepMind's Deep Q-learning playing Atari
Breakout](https://www.youtube.com/watch?v=V1eYniJ0Rnk&vl=en)

In a certain environment, the RL agent can take an action. The action can lead
the agent to a new state (possibly the same state), and it will receive a
reward as the result of taking the action (possibly none).

The rules for how you choose those actions are called policy.

#### State-Value Function and Action-Value Function
- state-value function: `V(s)`: how good is a state for an agent to be in.
- action-value function `Q(s, a)`: how good it is for an agent to pick action a
while being in state s. The "Quality" of a certain action in a given state.

#### Q-learning
Learn the action-value function, aka the Q function by interacting with the
environment.

#### Deep Q-learning
The Q-table can be very big. So we may want to use Neural Networks to
approximate the Q values.

#### Policy Gradient
##### REINFORCE Algorithm
![policy gradient](https://cdn-images-1.medium.com/max/1600/1*YQqZyAJ1QehPXFW36TKwmw.png)
- Ronald Williams. Simple statistical gradient following algorithms for
connectionnist reinforcement learning. In Machine Learning, 1992.

#### Comparing to Q-learning?
- [Deep Q Network vs Policy Gradients - An Experiment on VizDoom with
Keras](https://flyyufelix.github.io/2017/10/12/dqn-vs-pg.html)

Policy Gradient is a more direct approach, and it is generally believed to be
able to apply to a wider range of problems.

#### Variance Reduction
- [Understanding Actor Critic Methods and
A2C](https://towardsdatascience.com/understanding-actor-critic-methods-931b97b6df3f)

##### Advantage Actor Critic (A2C)
- Advantage Function: using the `V` function as the baseline function, we
subtract the `Q` value term with the `V` value. Intuitively, this means how much
better it is to take a specific action compared to the average, general action
at the given state.

#### Pointer Networks
![Ptr-Net](https://cdn-images-1.medium.com/max/1600/1*ztyKI9gryzcu-26PdHGRWg.png)
- [Introduction to pointer networks](http://fastml.com/introduction-to-pointer-networks/)
- [Pointer Networks](https://medium.com/@sharaf/a-paper-a-day-11-pointer-networks-59f7af1a611c) Amr Sharaf

The number of target classes in each step of the output depends on the length of the input, which is variable.

### Solving TSP: Implementation 
- [Michel Deudon](https://github.com/MichelDeudon/encode-attend-navigate/blob/master/code/Neural_Reinforce.ipynb)
