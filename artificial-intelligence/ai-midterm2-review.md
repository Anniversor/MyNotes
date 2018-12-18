# AI Midterm2 Review

## Midterm2 Review

### Spring 12 midterm2

#### V-Learning and Q-Learning:

$$
Q_{k+1}(s, a) = \sum_{s'}T(s, a, s')[R(s, a, s') + V_k(s')] \\
V_{k+1}(s) = \max Q(s, a)
$$

Basically, $Q​$ is just the expected value based on the action $a​$, and $V​$ is just the optimal value of $Q​$.

Why we don't want to use V-iteration: it's relatively slow because it needs to compute all the Q-values and V-values. But in fact Q-value is the determined factor of $V$, so we use Q-iteration to compute the optimal $Q$.

For Q-iteration, we can write that:

$$
Q_{k+1}(s, a) = \sum_{s'}T(s,a,s')[R(s,a,s')+ \max_{a'}Q_k(s',a')]
$$

It's just derived from the two equations above.

So after $i$ iterations, the policy we derive is that:

$$
\pi_i(s) = argmax_{a} Q_i(s, a), \text{for every state s}
$$

This equation just let us know how to choose action $a$ to let $V\_i\(s\)$ to be the maximum.

#### Some Probabilities

**Chain rule:** $$P(x_1, x_2,...,x_n) = \Pi_i P(x_i\vert x_1,... x_i-1)$$

**The whole probability**: $$P(x1) = \sum_{x_i \neq 1} P(x_1, x_2,...,x_n)$$

**Conditional Probability transformation using equations above:**

![image-20181218012622278](https://ws4.sinaimg.cn/large/006tNbRwly1fyavrbale1j30ty0843zt.jpg)

Basically first use the whole probability to convert and then use chain rule to get things that we can compute using the probabilities that have been given in the problems.

\*\*!!\*\* You should first look at the graph that is given and determine wether two variables are independent or conditionally independent.

**Bayes Networks and Sampling**

Nothing is hard, just review slides 19 and 20 and the homework 4.

#### Problems:

Why all the false should be "Cannot be determined" ?

