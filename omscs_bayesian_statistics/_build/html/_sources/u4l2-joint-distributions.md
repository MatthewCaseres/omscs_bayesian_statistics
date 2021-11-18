# Joint Distributions

## Defining Joint Distributions

Consider a random variable $X$ that is a vector of several other random variables, $X_1,X_2,...,X_n$.

$$X = (X_1,X_2,...,X_n)$$

We can generalize the pdf and cdf to this random variable -

$$\text{pdf} = f(x_1,x_2,...,x_n), \text{cdf}=F(x_1,x_2,...,x_n)$$

We pay special attention to the two dimensional case, $X=(X_1,X_2)$.

## Conditional distribution

Sometimes random variables depend on each other. More formally -

$$
X_1 = \begin{cases}
   1 \text{ if grade is an A} \\
  0 \text{otherwise }
\end{cases}
$$

$$
X_2 = \begin{cases}
1 \text{ if studiying over 15 hours a week} \\
0 \text{ otherwise }
\end{cases}
$$

$$
\text{What is } P(X_1 = 1) \text{ if } P(X_2 = 1)?
$$

There is notation for this

$$P(X_1=1|X_2=1) = P(X_1 = 1) \text{ if } P(X_2 = 1)$$

The | in the probability means it is a **conditional probability**.

This concept works for continuous distributions as well, denoted $f(x_1|x_2)$.

### Defining the conditional distribution

The conditional distribution is the probability that both of the things happened divided by the probability of the conditional.

$$
\begin{align}
p(x_1|x_2)\stackrel{\text{def}}{=} \frac{p(x_1,x_2)}{p(x_2)} \text{ for discrete} \\
f(x_1|x_2)\stackrel{\text{def}}{=} \frac{f(x_1,x_2)}{f(x_2)} \text{ for continuous}
\end{align}
$$

## Marginal distributions

Suppose we have $X=(X_1,X_2)$ but we really are only interested in $X_1$. How can we deal only with that? This is called the **marginal distribution** of $X_1$.

$$
\begin{align}
p(x_1)\stackrel{\text{def}}{=} \sum_{x_2 \in \text{Range}(X_2)}{p(x_1,x_2) }  \text{ for discrete} \\
f(x_1)\stackrel{\text{def}}{=} \int_{-\infty}^{\infty} f(x_1,x_2)dx_2 \text{ for continuous}
\end{align}
$$

## Discrete example

Prof. Brani Vidakovic shows us the marginals and conditional probabilities of the following distribution. Summing the rows gives the marginals for $X$ and summing the columns gives the marginals for $Y$. On the right we can see some calculations for conditionals.

![](./images/discrete-marginals.png)

## Continuous example (normal marginals)

### f(y)

This is sort of tricky, the trick is that completing the square in the exponent allows the integral to be broken up into two parts,

- A normal distribution depending on $x$
- A normal distribution not depending on $x$

So when we integrate over $x$ to find $f(y)$ the normal distribution depending on $x$ just turns to 1 and the other distribution remains.

![](./images/continuous-marginal-y.png)

### f(x)

The idea is the same for the marginal distribution of $x$

![](./images/continuous-marginal-x.png)

### Conditional distributions

We know $f(x,y)$ and $f(y)$ so we can compute $f(x|y) = \frac{f(x,y)}{f(y)}$

![](./images/continuous-conditional.png)

## Continuous example (independent)

![](./images/continuous-conditional-indep.png)

Independence helps because you can bring out part of the integral as a constant.
