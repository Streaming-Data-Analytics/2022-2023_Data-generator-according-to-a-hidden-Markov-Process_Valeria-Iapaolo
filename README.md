Data generator according to a hidden Markov Chain
============

## Part 1
The aim of this notebook is to generate data according to a Markov Chain with three states. To each state we assign a Gaussian distribution with mean $\mu_i$ and variance $\sigma_i^2$ with $i=0,1,2$. A little bit of notation: we call $S_0$, $S_1$, $S_2$ the three states and $p_{ij}$ the probability of going to state $j$ starting from state $i$. The states are such that
$$S_i \sim \mathcal{N}(\mu_i, \sigma_i^2)  $$     
for  $i=0,1,2$.

## Part 2
In part 1 we created some simulated data stream according to a Markov Chain: each time we leave a state we have a concept drift. The aim of part 2 is to test the concept drift detectors seen during the course on the generated data. The goal is to detect that a drift has occured each time we leave the current state.

## Part 3
The aim of this part is to understand if there is a time dependence between datapoints of the sequences generated until now. We will explore this dependence through the autocorrelation plot and the partial autocorrelation plot. <br>
Let's see the idea behind these two concepts:

- *Autocorrelation function* (**ACF**): at lag k, it is the correlation between values ​​in the series that are separated by k intervals.
- *Partial autocorrelation function* (**PACF**): at lag k, it is the correlation between the values ​​in the series that are separated by k intervals, taking into account the values ​​of the intervals in between. The key difference with respect to ACF is the exclusion of ***indirect correlations*** in the calculation.
