1. Definition
2. Cumulative Distribution Function (c.d.f)
3. Properties of c.d.f
4. N/A
5. Probability Mass Function (p.m.f)
6. Properties of p.m.f
7. Continuous Random Variable
8. Probability Density Function
9. Properties of p.d.f.
10. Distribution of functions of a r.v. - c.d.f. technique
11. One-to-One Tranformation of a continous r.v.
12. One-to-One Transformation of a discrete r.v.
13. Probability Integral Transformation

# Summary
##1. Definition

A random vairalbe is a function from $S$ to $R$. $X: S \rightarrow R$ in which $P(X \leq x)$ always exists for $\forall x \in R.$

##2. Cumulative Distribution Function (c.d.f.)

The c.d.f. or a r.v. is defined by $F(x) = P(X \leq x), x \in R$.
$F(x) = \mathbb R [0,1].$

##3. Properties of c.d.f.
(1) $F$ is non-decreasing


## 5. Probability Mass Function (p.m.f.)
If $x$ is discrete, the p.m.f. of $x$ is 
$$
f(x)=P(X=x)=F(x) - \lim_{\epsilon \rightarrow 0^+ }F(X-\epsilon) = 
F(x) - \lim_{a \rightarrow x^- }F(a)
$$

##6. Properties of p.m.f.
$f$ is a p.m.f. for some discrete r.v. if
$$
(1) \hspace{0.5cm} f(x) = 0 \\
(2) \hspace{0.5cm} \sum_{x \in A} f(x) = 1\\
\text{Note: }\sum_{x \in A} f(x) = \sum_{\forall x_i \in A}P(X=x_i) = P(\cup_{i=1}^{\infty}{ \{X=x_i\} } = P(S) = 1
$$

##7. Continous Random Variables
If $F(x)$ is a continous function $\forall x \in \mathbb R$ and $F$ is differentiable except possibly at countable many points, then $X$ is a continous r.v.

##8.Probability Density Function(p.d.f.)
If $X$ is a continuous r.v. w/ c.d.f. $P(x)$, then the p.d.f. of $X$ is
$$
F'(x) = \frac{d}{dx}F(x).
$$
If $F(x)$ is differentiable at $x$,  and otherwise we define $f(x) = 0$.
$A=\{  x:f(x)>0 \}$ is the support set of $X$.

##9. Properties of p.d.f.
$f$ is the p.d.f. for some continous random variables $X$ iff
\begin{align*}
(1) & \hspace{0.5cm} f(x) \geq 0 \\
(2) & \hspace{0.5cm} \int_{-\infty}^{\infty} f(x)dx = 1 \\
(3) & \hspace{0.5cm} f(x) = \lim_{h \rightarrow 0} \frac {F(x+h) - F(x)}{h} \tag{if the limit exists} \\
(4) & \hspace{0.5cm} F(x) = \int_{- \infty}^{\infty}f(t)dt \tag{for $x \in \mathbb R$} \\
(5) & \hspace{0.5cm} P(a < x \leq b) \\
& = P(X \leq b) - P(X \leq a) \\ 
& =\int_{-\infty}^{b}f(t)dt - \int_{-\infty}^{a}f(t)dt  \\
& = \int_{a}^{b}f(t)dt \\
(6) & \hspace{0.5cm} P(X=b) = 0 = \int_b^bf(t) dt \\
(7) & \hspace{0.5cm} P(a < X \leq b) = P(a \leq X \leq b) = P(a \leq X < b) = P(a < X < B) \\ 
& (\text{this is not true for discrete r.v.})
\end{align*}

##10.Distribution of functions of a r.v. (c.d.f. technique)
Suppose $X$ is a continous r.v. with p.d.f. $f$ and c.d.f. $F$ , and we wish to find the p.d.f. of the r.v. $Y=h(x)$

##11. One-to-One Transformations fo a continuous r.v.
Suppose $X$ is a continuous r.v. with p.d.f. $f$ and $A={x:f(x)>0}$ and $Y=h(x)$ where $h$ is one-to-one. Let $y$ be the p.d.f. of $Y$, then 
$$
g(y) = f(h^{-1}(y)) \cdot \Bigg| \frac{d}{dh}h^{-1}(y)\Bigg| \hspace{0.5cm} y \in B \text{ where } B = \{ y: g(y) \geq 0 \}
$$

##12. One-to-One transformation of a discrete r.v.
Suppose $X$ is a discrete r.v. w/ p.m.f. $f$ and $A= \{ x \enspace | \enspace f(x) > 0 \}$ and $ Y = h(X)$ where $h$ is one-to-one. Then, the p.m.f of $Y $ is
$$
g(y) = P(Y=y) = f(h^{-1}(y)), \enspace  y \in B \text{ where } B = \{ y: g(y) \geq 0 \}\\
$$

##13. Probability Integral Transformation
If $X$ is a continuous r.v. w/ c.d.f. $F$ and $F$ is strictly increasing, then $Y=F(X) \sim uniform(0,1)  $

We want to generate $y_1,y_2,\cdots,y_n$ from $F.$
We first generate $x_1,x_2, \cdots, x_n$ from $Uniform(0,1)$, then 
Let $y_i = F^{-1}(x_i)$, then $y_1,y_2, \cdots, y_n \sim F$



## Example
If $Z \sim N(0,1)$, find the p.d.f. of $Y=Z^2$

###Proof:
Let $F'(z)=f(z) = e^{-z^2/2}$ 
\begin{align}
G(y) & = P(Y \leq y) \\
& = P(Z^2 \leq y) \\
& = P(-\sqrt{y} \leq z \leq \sqrt{y}) \\
& = \int_{-\sqrt{y}}^{\sqrt{y}} \frac {1} {\sqrt{2\pi}} e^{-z^2/2} dz \tag{even function}\\
& = \frac {2} {\sqrt{2\pi}}\int_0^{\sqrt{y}} e^{-z^2/2}dz \\
=& \frac {2} {\sqrt{2\pi} } \int_0^{\sqrt{y}} f(z)dz \\
\\
\\
g(y) &= G'(y) \\
& = \frac{d}{dy} \frac {2} {\sqrt{2\pi} } \int_0^{\sqrt{y}} f(z)dz\\
& = \frac{2}{\sqrt{2\pi} } \frac {d}{dy} \Bigg[F(\sqrt{y}) - F(0) \Bigg] \\
& = \frac{2}{\sqrt{2\pi} }  \Bigg[  f(\sqrt{y}) \cdot \frac{d}{dy}(\sqrt{y}) - f(0)\cdot \frac{d}{dy} 0 \Bigg] \tag{chain rule} \\
& = \frac{2}{\sqrt{2\pi} } \Bigg[e^{-({\sqrt{y}})^2/2} \cdot \frac{1}{2\sqrt{y}} - 0 \Bigg] \\
& = \frac {1}{\sqrt{2 \pi y}} \cdot e^{-y/2} \hspace{1cm} for \hspace{1cm} y >0
\end{align}
Since $G(y)$ is c.d.f, $g(y)$ is p.d.f.
$$
Y \sim \chi(0,1)
$$