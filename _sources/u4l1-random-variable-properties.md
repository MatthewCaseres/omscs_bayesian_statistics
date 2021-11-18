# Random Variable Properties

## Expectation and moments

### Expectation

The expectation of a random variable $X$ is $E[X]$

$$
\begin{align*}
   E[X] &= x_1p_1 + x_2p_2 + ... + x_np_n + ... \text{ (for discrete)} \\
   &=\int_{\mathbb{R}} x \cdot f(x)dx \text{ (for continuous)}
\end{align*}
$$

### kth moment

The $k^{th}$ moment of a random variable $X$ is $E[X^k]$

$$
\begin{align*}
   E[X] &= x_1^kp_1 + x_2^kp_2 + ... + x_n^kp_n + ... \text{ (for discrete)} \\
   &=\int_{\mathbb{R}} x^k \cdot f(x)dx \text{ (for continuous)}
\end{align*}
$$

### General functions

For a general function $\varphi$ -

$$
\begin{align*}
   E[X] &= \varphi (x_1)p_1 + \varphi (x_2)p_2 + ... + \varphi (x_n)p_n + ... \text{ (for discrete)} \\
   &=\int_{\mathbb{R}} \varphi (x) \cdot f(x)dx \text{ (for continuous)}
\end{align*}
$$

## Variance and standard deviation

The **variance** is a measure of the spread of a distribution.

$$
\begin{align*}
   \text{Var}(X) &\stackrel{\text{def}}{=} E[(X-E[X])^2] \\
   &=E[X^2]-E[X]^2
\end{align*}
$$

The professor doesn't prove the jump from line 1 to line 2, but it involves some properties of expectation.

The **standard devation** is $\sigma_X = \sqrt {Var(X)}$

**Exponential distribution example**: If $X \sim \text{Exp}(\lambda)$ then $\text{Var}(X) = \frac{1}{\lambda^2}$ and $\sigma_x = \frac{1}{\lambda}$

## Quantiles

$\xi_p$ is the $p^{th}$ quantile of distribution $F$ if $F(\xi_p) = p$.

$$\xi_p = \inf(\{x|\sum_{x_i \leq x}p_i \geq p\}) \text{ (if discrete)}$$
$$\xi_p = \int_0^{\xi_p}f(x)dx = p \text{ or } F^{-1}(p) = \xi_p \text{ (if continuous)}$$

### Special quantiles

$$\text{Median} \stackrel{\text{def}}{=} \xi_{1/2} \text{ (50\% percentile, 0.5-quantile)}$$
$$Q_1, Q_3 \stackrel{\text{def}}{=} \xi_{1/4}, \xi_{3/4}  \text{ first and third quartiles}$$

## The mode

The **mode** is the most frequent/likely value.

- For continuous distributions this is the largest value.
- For discrete distributions the is the value $x_i$ that maximizes $P(X=x_i)$

**example:** If $X \sim \text{Exp}(\lambda)$ the median is $\frac{\log(2)}{\lambda}$ and the mode is $0$.
