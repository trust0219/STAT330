1. Expectation
2. Expectations for a function of X
3. $E[ag(x) + bh(x)] = a \cdot E[g(x)] + b \cdot E[h(x)] $
4. Special Expectaions
  (1) Variance
  (2) $K^{th} -momentdf$
  (3) $K^{th} -moment $ (about the mean)
  (4) $K^{th} - factorial\hspace{0.3cm}moment$
5. $Var(aX+b) = a^2 Var(X)$
6. Markov's Inequality
7. Chebyshev's Inequality
8. Degenerate Distribution
9. Variance Stabilizing Tranformation
10. ----- NO EXAM
  

## 1. Expectation
- Discrete R.V. with p.m.f $\enspace f(x)$ and support set $A$, then 
$$
E(X) = \sum_{x \in A} x \cdot f(x)
$$
provided the sum converges absolutely, i.e.
$$
E [\;|\>X \>| \;] = \sum_{x \in A} \;|\>x \>| \; \cdot f(x) < \infty
$$
if $E[|X|] = \infty$, then $E(X)$ doesn't exist.
- Continous R.V. with p.d.f. $f(x)$ and support set $A$, then
$$
E(X) = \int_{-\infty}^{\infty} x \cdot f(x) \; dx
$$
provided the sum converges absolutely, i.e.
$$
E [\;|\>X \>| \;] = \int_{-\infty}^{\infty} \;|\>x \>| \; \cdot f(x) < \infty
$$


##2. Expectations of a function of $X$
If $X$ is discrete, 
$$
E[h(X)] = \sum_{x \in A} h(x) \cdot f(x) \tag{i.e. weighted average}
$$
- Provided that $E(\;|\;h(x)\;|\;) < \infty$, if $X$ is continous, 
$$
E(\;|\;h(x)\;|\;) = \int_{-\infty}^{\infty} h(x) \; f(x) \; dx
$$

## 3. $ E[ag(x) + bh(x)] = a \cdot E[g(x)] + b \cdot E[h(x)] $
Provided that $E(\;|\;h(x)\;|\;) < \infty$, if $X$ is continous 

## 4. Special Expectations
(1) Variance
$$
\sigma^2 = Var(X) = E(X^2) - [E(X)]^2
$$

(2) $k^{th} $moment
$$
E(X^k)
$$

(3) $k^{th} $moment (about the mean)
$$
E\big[(X- \mu )^k \big]
$$

(4) $k^{th} $ factorial moment
$$
E\big[ X^{(k)} \big] = E \big[  X \cdot (X-1) \cdots (X-k+1)  \big]
$$


## 5. $Var(aX+b) = a^2 Var(X)$

## 6. Markov's Inequality
$$
P\big( |X| \geq c \big) \leq \frac{E \big|X \big|^k}{C^k} \tag{$\forall \; k,c > 0$}
$$


## 7. Chebyshev's Inequality
Suppose $X$ is a r.v. w/ finite mean $\mu$ and finite variance $\sigma^2$. Then, $\forall k>0,$
$$
P\big( |X-\mu|  \geq  k \sigma \big) \leq \frac{E\big(  X - \mu  \big)^2}{\big( k\sigma \big) ^2} = \frac{\sigma^2}{k^2 \sigma^2} = \frac{1}{\sigma^2}
$$

## 8. Degenerate Distribution
If $\mu = E(X), \sigma^2 = Var(X) = 0,$ then we have 
$$
P(X=\mu) = 1
$$


## 9. Variance Stabilizing Transformation
- R.V. $X$
- $E(X) = \theta$
- $Var(X) = \sigma^2(\theta)$

We aim to find $Y = g(X) \enspace $ s.t. $\enspace Var(g(X)) \enspace$ is a constant.
$$
Y = \alpha + \beta z + \epsilon \\  
E(\epsilon) = 0 \enspace \Rightarrow \enspace E(Y) = \alpha + \beta z\\
Var(\epsilon) = \sigma^2 \Rightarrow Var(Y) = \sigma^2 \\
$$


$$
Y = g(x) \approx g(\theta) + g'(\theta)(X-\theta) \\
E(Y) \approx g(\theta) + g'(\theta)(\theta - \theta)  \tag{form: $Y = \alpha + \beta z + \epsilon$} = g(\theta) \\
Var(Y) \approx \big[g'(\theta)\big] ^2\cdot Var(X-\theta) =  \big[g'(\theta)\big] ^2 \sigma^2(\theta) = \big[ g'(\theta) \cdot \sigma(\theta) \big] ^2
$$
If we want $Var(Y)$ to be a constant, we just need $g'(\theta) \cdot \sigma(\theta) \approx \text{constant}.$ 
That is, $g'(\theta) = \frac {k}{\sigma(\theta)}$ where $k$ is a conveniently chosen constant.