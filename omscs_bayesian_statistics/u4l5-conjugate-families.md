# Conjugate families

## Definition

In our previous example we saw that with a normal likelihood and a normal prior -

$$x|\theta \sim N(\theta, \sigma^2) \text{ with } \sigma^2 \text{ known }$$
$$\theta \sim N(\mu, \tau^2)\text{ with } \mu,\tau^2 \text{ elicited }$$

that the posterior was also normally distributed

$$\theta|x \sim N(\frac{\tau^2}{\sigma^2 + \tau^2}x + \frac{\sigma^2}{\sigma^2 + \tau^2}\mu, \frac{\sigma^2\tau^2}{\sigma^2 + \tau^2})$$

Generally if for a likelihood function $f$, the prior $\theta$ and posterior $\theta | x$ have the same distribution, then the pair $(f, \pi)$ **is conjugate**.

### Normalizing

If we know that $(f, \pi)$ is conjugate we do not need to calculate the normalizing constant

$$m(x) = \int_\Theta h(x,\theta)d\theta$$

This integral can be difficult, and since we know the form of $\pi(\theta|x)$ (even if it isn't normalized)

$$\pi(\theta|x) = \frac{f(x|\theta)\pi(\theta)}{m(x)} \propto f(x|\theta)\pi(\theta)$$

we can ignore $m(x)$ altogether and choose the correct normalizing constant for the distribution proportional to $f(x|\theta)\pi(\theta)$.

## Binomial likelihood, beta prior
