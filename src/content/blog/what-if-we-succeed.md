---
slug: what-if-we-succeed
publishDate: 2020-07-25T15:49:30Z
author: Ranjani Mani
title: What if we Succeed? 
excerpt: Recent years progress in artificial intelligence has prompted renewed interest in a question posed by Russell and Norvig : What if we succeed? If and when AI researchers succeed at the goal of designing machines with cross-domain learning and decision-making capabilities that rival those of humans, the consequences for science, technology, and human life are  ... 
category: 13
---

##### Recent years progress in artificial intelligence has prompted renewed interest in a question posed by Russell and Norvig : What if we succeed?

![Technological Singularity Source: Kurzweil 2006 ](https://i0.wp.com/ranjanimani.com/wp-content/uploads/2020/07/Technological-Singularity-Source-Kurzweil-2006.png?resize=850%2C420&ssl=1)

Technological Singularity Source: Kurzweil 2006

If and when AI researchers succeed at the goal of designing machines with cross-domain learning and decision-making capabilities that rival those of humans, the consequences for science, technology, and human life are likely to be large.

> **What if we get to the point of Superintelligence where machines are better and smarter than us?**

I find a lot of cognitive dissonance in getting myself to accept the concept of singularity and the potential backlashes that may follow.

There are a bunch of companies and individuals who aren’t just asking these questions but going ahead in working in creating systems and checks in place to ensure the future isn’t science fiction we did not plan for.

This is really good paper I came across on [Alignment Machine Learning](https://intelligence.org/files/AlignmentMachineLearning.pdf) and it attempts to understand and expound on these thought.

**Complete article content credit to the authors of the paper.**

Russell talks about the potential that a system’s objective function _– may not be perfectly aligned with the values of the human race, which are (at best) very difficult to pin down;_ 

Any sufficiently capable intelligent system will prefer to ensure its own continued existence and to acquire physical and computational resources not for their own sake, but to succeed in its assigned task.

What really is the motivation for such research – In the long run, as ML and AI gain capabilities, humans will continue to place trust on these systems to make larger decisions. It becomes critically important thus that they act in accordance with the intentions of the operators and without posing a threat to the society at large.

Imagine designing a cure for Parkinson’s ‘_without doing anything drastic_‘. Teaching a kid what is ‘drastic’ is a learnt behavior. How do we translate this into machines?

> _Also, one of the key attractions of learning systems is that they can find clever ways to meet objectives that the programmers might not have thought of. It is thus a ‘feature’ of learning and not a ‘bug’._

‘Consider the challenge of designing robust objective functions for learning systems that are capable of representing facts about their programmers beliefs and desires. If the programmers learn that the systems objective function is mis-specified, then they will want to repair this defect. If the learner is aware of this fact, however, then it has a natural incentive to conceal any defects in its objective function, for the systems current objectives are unlikely to be achieved if the system is made to pursue different objectives.’

##### **How does this translate technically ? In trying to create what I am going to term as ‘safe AI’? There are two types of research that might help in this.** 

1. ##### **Research that makes it easier to specify our intended goals as ‘objective functions**
2. ##### **Research to design AI systems that avoid side effects and negative incentives even if the objective function is not completely met.**

As per this paper, Soares and Fallenstein (2014) refer to the former approach as _value specification_, and the latter as _error tolerance_.

This paper highlights 8 of these research areas based on these two approaches. A lot of companies in the ML community are currently working in this area. \[Ref – [OpenAI](https://openai.com/)\]

Some of these areas are based on value specification, some on error tolerance and some others on both. Also, there is a pre-requisite that the solutions that are proposed need to be applicable even in ML systems that are more capable than the ones that exist today.

Which implies that solutions that depend on the system’s ignorance of a certain fact discover able in the future or assumption of its inability to come up with a particular strategy would be unsatisfactory in the long run.

What are these 8 research areas?

#### **1\] Inductive ambiguity identification :** How can we train ML systems to detect and notify us of cases where the classification of test data is highly under-determined from the training data

### _“There is a need to build systems that keep humans ‘in the loop’ and recognize when they are (or aren’t) too inexperienced to make a critical decision”_

Consider a classic parable recounted by Dreyfus and Dreyfus (1992): The US army once built a neural network intended to distinguish between Soviet tanks and American tanks. The system performed remarkably well with relatively little training data so well, in fact, that researchers grew suspicious.

Upon inspection, they found that all of the images of Soviet tanks were taken on a sunny day, while the images of US tanks were taken on a cloudy day. The network was discriminating between images based on their brightness, rather than based on the variety of tank depicted. It is to be expected that a classifier, given training data, will identify very simple boundaries (such as brightness) that separate the data.

However, what we want is a classifier that can, given a data set analogous to the tank training set, recognize that it does not contain any examples of Soviet tanks on cloudy days, and ask the user for clarification. Doing so would likely require larger training sets and different training techniques. The problem of inductive ambiguity identification is to develop robust techniques for automatically identifying this sort of ambiguity and querying the user only when necessary

#### **2\] Robust human imitation**: How can we design and train ML systems to effectively imitate humans who are engaged in complex and difficult tasks?

* We essentially want the system to ‘consult a human operator for advice’ without actually providing that as a general purpose objective function.
* The high-level question here is: Can we define a measurable objective function for human imitation such that the better a system correctly imitates a human, the better its score according to this objective function?

#### **3\] Informed oversight**: How can we train a reinforcement learning system to take actions that aid an intelligent overseer, such as a human, in accurately assessing the systems performance?

* Consider an ML system trained to write original novels, using a corpus of human novels as training data. It might be quite a bit less intelligent than a human (according to many different intelligence metrics), but the human may still have a fair bit of trouble accurately evaluating the systems performance. For instance, it might be easy for the system to simply plagiarize a novel, and it might be hard for a human to check whether the novel was in fact plagiarized. (Perhaps the system used a simple rewriting scheme to make the plagiarism difficult to detect by a text search, but still easy to detect for a human comparing the novels side-by-side.) How do we make it easy for the human to assess the performance of an advanced ML system pursuing some particular task?

##### TL;DR – How can we train systems to not only take good actions, but take actions that can be accurately assessed by overseers?

#### **4\] Generalizable environmental goals**: How can we create systems that robustly pursue goals defined in terms of the state of the environment, rather than defined directly in terms of their sensory data?

* Many ML systems have their objectives specified in terms of their sensory data. For example, reinforcement learners have the objective of maximizing discounted reward over time where reward and/or loss are part of the systems precepts.
* While these sensory goals can be useful proxies for environmental goals, environmental goals are distinct: Tricking your sensors into perceiving that a sandwich is in the room is not the same as actually having a sandwich in the room

#### **5\] Conservative concepts**: How can a classifier be trained to develop useful concepts that exclude highly atypical examples and edge cases?

* Many of the concerns raised by Russell (2014) and Bostrom (2014) center on cases where an AI system optimizes some objective, and, in doing so, finds a strange and undesirable edge case.
* For example, if we task an AI system with creating screwdrivers, by showing it 10,000 examples of screwdrivers and 10,000 examples of non-screwdrivers, we might want it to create a pretty average screwdriver as opposed to, say, an extremely tiny screwdriver even though tiny screwdrivers may be cheaper and easier to produce.

#### **6\] Impact measures:** What sorts of regularizers incentivize a system to pursue its goals with minimal side effects?

* We would prefer a highly intelligent AI system to avoid creating large unintended side effects in pursuit of its objectives, and also to notify us of any large impacts that might result from achieving its goal. For example, if we ask it to build a house for a homeless family, it should know implicitly that it should avoid destroying nearby houses for materials a large side effect.

#### **7\] Mild optimization**: How can we design systems that pursue their goals without trying too hard, i.e., stopping when the goal has been pretty well achieved, as opposed to expending further resources searching for ways to achieve the absolute optimum expected score?

* Many of the concerns discussed by Bostrom (2014) in the book [Superintelligence ](https://www.goodreads.com/book/show/20527133-superintelligence)describe cases where an advanced AI system is maximizing an objective as hard as possible
* Perhaps the system was instructed to make only 1000 paperclips, and it uses every resource at its disposal and every trick it can come up with to make sure that it definitely made 1000 paperclips (and that its sensors didn’t have any faults)
* The problem of mild optimization is: how can we design AI systems and objective functions that, in this intuitive sense, don’t optimize more than they have to?

#### **8\] Averting instrumental incentives:** How can we design and train systems such that they robustly lack default incentives to manipulate and deceive the operators, compete for scarce resources, etc?

* This is the use-case that science fiction is made of. The apocalyptic ones at that. For example, if the system is rewarded for shutting down when the humans want it to shut down, then the system has incentives to take actions that make the humans want to shut it down
* A system that believes that the operators (and only the operators) possess knowledge of the right objective function might be very careful in how it deals with the operators, and this caution could counteract potentially harmful default incentives

Let us just consider one of them to understand the complication and need for designing such systems. These are traits that are inherent in humans. Learnt behavior that my 2.5 year old has probably already picked up from us.

Mild optimization: How can we design systems that pursue their goals without trying too hard, i.e., stopping when the goal has been pretty well achieved, as opposed to expending further resources searching for ways to achieve the absolute optimum expected score?

We know perfect is the enemy of good. We as people probably have different radius’ in terms of how long we continue to persist on a activity in alignment with the ROI it brings in. There is clearly a dial in our heads that tells us when and where to stop. The word is [satisficing](https://en.wikipedia.org/wiki/Satisficing).

There is clearly a lot of work that is currently happening in each of these areas. Something I hope to cover in part 2 of this post.

##### The larger question remains – How do we teach a machine to learn traits that is so critically important in what makes us, us.

![](https://i0.wp.com/ranjanimani.com/wp-content/uploads/2020/07/EthicsofAI.png?resize=1000%2C563&ssl=1)

https://www.kuppingercole.com/blog/small/the-ethics-of-artificial-intelligence