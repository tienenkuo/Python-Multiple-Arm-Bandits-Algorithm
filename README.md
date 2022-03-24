# Multiple-Arm-Bandits-Algorithm
> Implement three different algorithms for the multi-armed bandit problem and simulate their performance

## A/B Testing Recap
A/B testing relies on classic statistical test for statistical significance. When we come up with a new product feature, we probably want to test whether it is useful before launching it to the entire user base. The test involves two groups: a treatment group (who have access to the new feature) and a control group.The difference between the groups is tested for statistical significance.
A balanced AB test would allocate equal amount of traffic to each group, until reaching sufficient sample size. However, we cannot adjust traffic allocation during the test based on what is observed. So the disadvantage of A/B testing is obvious: if the treatment group is clearly superior, we still have to spend lots of traffic on the control group, in order to obtain statistical significance

## Multi-armed Bandit
Whereas A/B testing is a frequentist approach, we can also conduct the test from the Bayesian way. It is understandable that once we see one treatment is clearly better, we want to add more users to that treatment right away. Multi-armed bandit experiment makes this possible in a controlled way.
The foundation of the multi-armed bandit experiment is Bayesian updating. Each treatment (called “arm”, see class definition below) has a probability of success, which is modeled as a Bernoulli process. The probability of success is unknown, and is modeled by a Beta distribution. As the experiment continues, each arm receives user traffic, and the Beta distribution is updated accordingly. 

Resource: [Towards Data Science](https://towardsdatascience.com/beyond-a-b-testing-multi-armed-bandit-experiments-1493f709f804)
