# Bayesian prediction

Recall that the marginal distribution $m(x) = \int f(x|\theta) \pi(\theta) d\theta$ which is sometimes called the **prior predictive distribution**.

We have a **posterior predictive distribution**:

$$f(x_{n+1}|x_1,...,x_n) = \int f(x_{n+1} | \theta) \pi(\theta | x_1,...,x_n)d\theta$$

A **predictive mean**

$$\hat{X}_{n+1} = \int x_{n+1} \cdot f(x_{n+1}|x_1,...,x_n) dx_{n+1} = E^fX_{n+1}$$

A **predictive variance**

$$\int(x_{n+1} -\hat{X}_{n+1})^2  \cdot f(x_{n+1}|x_1,...,x_n) dx_{n+1}$$

## Example

![](./images/predictive.png)
![](./images/predictive-2.png)
