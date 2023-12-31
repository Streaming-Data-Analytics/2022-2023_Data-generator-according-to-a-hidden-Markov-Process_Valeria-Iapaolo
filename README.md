Data generator according to a hidden Markov Chain
============

## Part 1
The aim of this notebook is to generate data according to a Markov Chain with three states. To each state we assign a Gaussian distribution with mean $\mu_i$ and variance $\sigma_i^2$ with $ i=0,1,2 $. A little bit of notation: we call $S_0$, $S_1$,$S_2$ the three states and $p_{ij}$ the probability of going to state $j$ starting from state $i$. The states are such that
$$S_i \sim \mathcal{N}(\mu_i, \sigma_i^2)  $$     
for  $ i=0,1,2 $.

