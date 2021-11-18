# Background

## Reverend Thomas Bayes

Professor Vidakovic gives details on the life and work of Reverand Thomas Bayes. I am not sure we will be tested on any of this, but the curious student can find details on [wikipedia](https://en.wikipedia.org/wiki/Thomas_Bayes).

- Lecture 1 covers the wikipedia section on Bayes' biography
- Lecture 2 covers the wikipedia section on Bayes' famous essay

## Classical vs. Bayesian

## Classical vs. Bayesian statistics

![](./images/classical-vs-bayesian.png)

### Coin flips example

Suppose we flip a coin 10 times and get 10 tails.

If the probability of getting heads is $p$ then the probability of this happening is $(1-p)^{10}$. The probability of this happening is maximized when $p=0$, and the frequentist approach will estimate that $p=0$.

In a Bayesian approach we find the probability distribution of our unknown parameter given some prior distribution. **We omit some details for now**.

We have an initial estimate of the probability distribution of $p$ as being uniform on the interval $[0,1]$. We update this estimate with the likelihood from our experiment and get a new probability density function

$$11(1-p)^{10}$$

We can now get more meaningful information about the probability distribution like the

- mean = 1/12
- median = $(-.5)^{\frac{1}{11}}+1$ = .061069
- mode = 0

Bayesian statistics gives us a full distribution of a parameter of interest.

## FDA Guidance

Professor Vidakovic summarizes [FDA guidance on the use of Bayesian statistics](https://www.fda.gov/media/71512/download).

The FDA is advocating for the use of Bayesian methods in development of medical devices.

- Prior information from other devices with similar mechanisms of action is available and can be used by Bayesian methods.
- Bayesian approaches may be simpler and less burdensome.
- Prior information may reduce the required size of the trial.
- Size of a trial can be reduced by early stopping
  - Early stopping is more controversial when using frequentist methods compared to Bayesian
- Multiplicity problems are easier when using Bayesian approaches.
- Missing data is handled more gracefully by Bayesian approaches.
- Unlimited looks at the data are okay in Bayesian approaches, more complicated in frequentist approaches and involve "Alpha spending"

The ability to stop the trial early due to **inferiority** (the method is not good) or **superiority** (the method shows itself to be good) reduces the human and economic costs of medical trials.
