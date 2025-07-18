# Questions

1- What is the difference between probability and measure?

2- How many ways are there to bound two distributions?

3 - How many notions of distance are there between probability distributions?

4- What is rate of convergence?
5 -  what are the steps for defining a distance function?
5-1 The fix a class of functions. we can pick our favorite class of functions, for example, the class of Lipschitz functions, the class of bounded functions, the class of continuous functions, etc.
5-2 Then for each of these functions, we compute the expectation of the function for the two distributions.
5-3 we look at the worst case of the difference between the two expectations. which is the supremum of the absolute value of the difference between the two expectations.
$X \sim F_1$ and $Y \sim F_2$ are two random variables with distributions $F_1$ and $F_2$ respectively. The distance function is defined as:
$$d(F_1, F_2) = \sup_{f \in \mathcal{F}} \left| \mathbb{E}_{F_1}[f(X)] - \mathbb{E}_{F_2}[f(Y)] \right|$$

where $\mathcal{F}$ is the class of functions we fixed in step 5-1.
6- Show that $d(F_1, F_2)$ is distance.


---
## Example of Distances in this framework
1. **Kolmogorov metric:** in Kolmogorov metric, the class of functions is the class of step functions. 
$$d_k(X, Y) = \sup_{f \in \mathcal{F}_k} \left| \mathbb{E}_{F_1}[f(X)] - \mathbb{E}_{F_2}[f(Y)] \right|$$
$$= \sup_{x \in \mathbb{R}} \left| \mathbb{P}(X \leq x) - \mathbb{P}(Y \leq x) \right|$$.

where $\mathcal{F}_k  = \{\mathbb{1}_{\{.\leq x\}}: x \in \mathbb{R}\}$ is the class of step functions.
it is the function that upto x is zero and after x is one. Essentially in kolmogorov metric, we are looking at the supremum of the absolute difference between the cumulative distribution functions (CDFs) of the two distributions. we look at the difference between the CDF of $F_1$ and the CDF of $F_2$ at every point $x$ in $\mathbb{R}$, and take the supremum of these differences.

**Central Limit Theorem** talks about convergence in kolmogorov metric. 

7- What is the difference between distance and metric?

