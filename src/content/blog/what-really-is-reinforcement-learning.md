---
slug: what-really-is-reinforcement-learning
publishDate: 2020-07-14T17:26:37Z
author: Ranjani Mani
title: What really is Reinforcement Learning 
excerpt: I started re-reading this book (Drive – Daniel Pink) recently on what really motivates people and how our paradigms of learning, fulfillment and intrinsic rewards are changing rapidly. It reminded me of reinforcement learning (in the context of ML and AI). A concept I have attempted to deconstruct below. Machine Learning (ML) focuses on creating  ... 
category: 13
---

I started re-reading this book ([Drive – Daniel Pink](https://www.goodreads.com/book/show/6452796-drive)) recently on what really motivates people and how our paradigms of learning, fulfillment and intrinsic rewards are changing rapidly. It reminded me of reinforcement learning (in the context of ML and AI). A concept I have attempted to deconstruct below.

Machine Learning (ML) focuses on creating intelligent programs or ‘agents’ through the process of ‘learning’.

![](https://i0.wp.com/ranjanimani.com/wp-content/uploads/2020/07/Reinforcement_learning_diagram.svg_-1.png?resize=250%2C242&ssl=1)

**What is Reinforcement Learning?**

1. **Reinforcement Learning (RL) is one approach of ML** in which the agent learns through interaction with its environment and through the results of the interactions.
2. This is essentially a **mimicry of how humans learn** \[side note – quoting Alan Turing – “Instead of trying to produce a program to simulate the adult mind, why not rather try to produce one which simulates the _child’s_?\]
3. In this, the algorithm allows the software agents to automatically determine the ‘ideal behavior’ within a specific context that ‘**maximizes its performance**‘ – **“Reinforcement learning is concerned with the problem of finding suitable actions to take in a given situation in order to maximize a reward.” \[[Ref](https://www.microsoft.com/en-us/research/people/cmbishop/?from=http%3A%2F%2Fresearch.microsoft.com%2Fen-us%2Fum%2Fpeople%2Fcmbishop%2Fprml%2F)\]**
4. **No specific goals** – The algorithms thus arent provided with explicit goals and end up learning them through trial and error (much like how we, as humans learn)
5. **Lets talk examples and use cases** – Reinforcement systems can be understood from the perspective of games which come with a clear objective that is awarded points. As shown in this [example](https://medium.com/machine-learning-for-humans/reinforcement-learning-6eacf258b265), say the mouse is looking at getting to a piece of cheese at the end of a maze (+1000 points) and gets an intermediate award of +10 points on the way (for say, water). There is also negative reinforcement in the form of electric shocks (-100 points). After exploring around a bit, the mouse may find a bunch of smaller rewards in form of water – but if it sticks around there it may miss the bigger award of the cheese at the end. It thus has to decide on a **trade-off between exploration/exploitation** (much like decisions we puzzle over). One strategy might be to take the best known action for a majority of the time (80%+) but occasionally explore newer options or directions in this case that may result in an unknown reward (even it if means walking away from the known and available reward i.e water in this case) \[ Here is a [paper](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching%5Ffiles/XX.pdf) from UCL related to ‘exploitation vs exploration’ but that deep-dive is for another article\] – This is referred to as the ‘[**epsilon-greedy strategy**](https://en.wikipedia.org/wiki/Multi-armed%5Fbandit)‘. Here epsilon refers to the percent of time that the agent takes a randomly selected action rather than the action that is most likely to maximize the reward given what it knows so far (that is the 20% minority route). We usually start with a high value of epsilon (i.e, a large % of time look at taking the unknown initially/exploration) but over time the mouse (or us) learn about the maze and learn about which results in a long term reward and reduce epsilon steadily (i.e – prefer the routes that are known) until it reaches 10% or lesser to exploiting what it already knows.![](https://i0.wp.com/thetrifecta.in/wp-content/uploads/2018/01/1_HvoLc50Dpq1ESKuejhICHg-300x147.png?resize=300%2C147)

[\[Image ref\]](http://rll.berkeley.edu/deeprlcourse-fa15/)

* ![](https://i0.wp.com/ranjanimani.com/wp-content/uploads/2020/07/Reinforcementlearning.png?resize=1024%2C552&ssl=1)

source – ML for humans

**To summarize**, RL is a ‘goal oriented’ algorithm where the learning happens not from a training set but from the agent’s interaction with the environment.

RL is considered to be the hope and driving force behind true AI given its immense learning potential.

Here is an immensely astounding (and slightly alarming) video of Google’s DeepMind AI that taught itself how to walk without any prior guidance.

**So how is RL different from other Machine Learning**? – RL does not have existing training data (like in most Supervised learning) and the agent learns from experience. It collects the training examples as it encounters them – through trial and error as it attempts them (‘this action was good, this was bad’) with the aim of maximizing long term reward. Here is a classification of different types of ML from [Analytics Vidhya](https://www.analyticsvidhya.com/blog/2017/01/introduction-to-reinforcement-learning-implementation/)![](https://i0.wp.com/thetrifecta.in/wp-content/uploads/2018/01/ml_types-300x191.png?resize=514%2C327)

It is thus clearly seen that unlike ‘Supervised Learning’, RL doesn’t have an ‘external supervisor’ which has and shares knowledge of the environment with the agent to complete the task.Â And unlike in ‘Unsupervised Learning’, RL has a mapping from the input to the output which is not present in Unsupervised learning. Unsupervised learning focuses on learning ‘underlying patterns’ in the provided training data. RL creates the data and learns through its attempts at maximizing the end reward.

* The [actions](http://www.cse.unsw.edu.au/~cs9417ml/RL1/introduction.html) thus can be summarized as follows – The **“cause and effect”** idea can be translated into the following steps for an RL agent:  
   1. The agent observes an input state  
   2. An action is determined by a decision making function (policy)  
   3. The action is performed  
   4. The agent receives a scalar reward or reinforcement from the environment  
   5. Information about the reward given for that state / action pair is recorded

**Where is RL used?** – RL problems are potentially those that can be solved without external supervision – complex problems where there appears to be no obvious or easily programmable solutions. Two main areas where the currently applications span are –

* **Game Playing** – Think Chess
* **Control Problems** – Say, Elevator scheduling

More details related to the use cases, deep-dive of the algorithms and techniques are covered in part 2 of the post.

**Here are some additional reading links-**

1. http://www.cse.unsw.edu.au/\~cs9417ml/RL1/introduction.html
2. https://www.techopedia.com/definition/32055/reinforcement-learning
3. https://www.analyticsvidhya.com/blog/2017/01/introduction-to-reinforcement-learning-implementation/
4. https://www.dropbox.com/s/e38nil1dnl7481q/machine\_learning.pdf?dl=0
5. https://www.analyticsvidhya.com/blog/2016/12/getting-ready-for-ai-based-gaming-agents-overview-of-open-source-reinforcement-learning-platforms/
6. http://rll.berkeley.edu/deeprlcourse-fa15/docs/2015.08.26.Lecture01Intro.pdf
7. http://rll.berkeley.edu/deeprlcourse-fa15/
8. https://medium.com/machine-learning-for-humans/reinforcement-learning-6eacf258b265
9. https://www.kdnuggets.com/2016/05/machine-learning-key-terms-explained.html/2
10. http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching\_files/XX.pdf