# Ingredients for Bayesian Inference

## Likelihood

We have several observations $X_1,...,X_n$ of a random variable that are independent and identically distributed (IID). We suppose they come from a distribution parameterized by $\theta$.

$$X_i \sim f(x_i| \theta), \text{ for } i=1,...,n$$

The joint distribution is

$$
\begin{align*}
f(x_1,x_1,...x_n|\theta) &= f(x_1|\theta) \cdot f(x_2 | \theta) ... f(x_n|\theta) \text{ by independence}\\ &= \prod_{i=1}^nf(x_i|\theta)
\end{align*}
$$

The **likelihood** function $L$ is a measure of how likely an outcome is for a particular value of $\theta$.

$$L(\theta|x_1,...,x_n) = \prod_{i=1}^n f(x_i| \theta)$$

### Likelihood Principle

The **likelihood principle** states that "all the evidence in a sample relevant to the model parameters is contained in the likelihood function" (from [Wikipedia](https://en.wikipedia.org/wiki/Likelihood_principle)).

### Example

$X_i$ have exponential distributions $\text{Exp}(\lambda)$ and are independent.

$$
X_1=2, X_2=3, X_3=1 \implies \\
L(\lambda|x_1,x_2,x_3) = \lambda e^{-2\lambda} \cdot \lambda e^{-3\lambda} \cdot \lambda e^{-\lambda} = \lambda ^3 e^{-6\lambda}
$$

In general for $n$ independent exponential distributions with parameter $\lambda$.

$$L(\lambda|x_1,x_2,...,x_n) = \lambda^ne^{-\lambda\sum_{i=1}^nx_i}$$

## Distribution of theta

Let $\theta$ be a parameter in $f(x|\theta)$.

A prior $\pi(\theta)$ is a distribution of $\theta \in \Theta$ where $\Theta$ is the set of possible parameters.

The joint distribution of $(X, \theta)$ is $h(x,\theta)$.

The marginal distribution of $X$ is

$$m(x) = \int_\Theta h(x,\theta)d\theta$$

## Bayes' Theorem

Just like there is a Bayes' Rule for events -

$$P(A \cap H_i) = P(A | H_i)P(H_i) = P(H_i|A)P(A)$$
$$\implies P(H_i|A) = \frac{P(A | H_i)P(H_i)}{P(A)}$$

We have a **Bayes' theorem** for the joint distribution of $(X, \theta)$, $h(x, \theta)$.

$$h(x,\theta)=f(x|\theta)\pi(\theta) = \pi(\theta|x)m(x) \implies$$
$$\pi(\theta|x) = \frac{f(x|\theta)\pi(\theta)}{m(x)} \text{ Bayes' Theorem}$$

## Example: normal likelihood, normal prior

Terminology

- **elicited** means that some assumptions are made before hand using prior information.
- **hyperparameters** are parameters of the distribution of the parameter.

We complete the square in the exponent to simplify the joint distribution $h(x,\theta)$. Below is the slide from unit 4, lecture 4. The expressions in the red circles are equivalent after some unpleasant but straightforward algebra.

![](./images/normal-likelihood-normal-prior1.png)

### Interpretation as weights

Notice that the posterior distribution $\theta | X$ has mean (median and mode) of $\frac{\tau^2}{\sigma^2 + \tau^2}x + \frac{\tau^2}{\sigma^2 + \tau^2}\mu$ where

- $x$ is observed
- $\mu$ is elicited

This is a weighted average

$$\frac{\tau^2}{\sigma^2 + \tau^2}x + \frac{\sigma^2}{\sigma^2 + \tau^2}\mu = w \cdot x + (1-w) \cdot \mu \text{ where}$$

$$w = \frac{\tau^2}{\sigma^2 + \tau^2} \text{ and } \mu = \frac{\sigma^2}{\sigma^2 + \tau^2}$$

Notice that

$$\tau^2 \gg \sigma^2 \implies w \approx 1 \text{ the posterior mean is close to x}$$
$$ \sigma^2 \gg \tau^2 \implies w \approx 0 \text{ the posterior mean is close to } \mu$$

Also notice that if our likelihood and prior are normal, that our posterior is normal. This means that our likelihood and prior are **conjugate**, the subject of the next lecture.
