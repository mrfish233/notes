# 12 Vector-Valued Functions and Motion in Space

## 12.1 Curves in Space and Their Tangents

A particle moves through space during a time interval $I$ is defined as function of its coordinates:

$$
x = f(t), \quad y = g(t), \quad z = h(t), \quad t \in I.
$$

The points $(x, y, z)$ make up the **curve** in space is called the particle's **path**. Its vector form is

$$
\textbf{r}(t) = \overset\rightharpoonup{OP}
= f(t) \textbf{i} + g(t) \textbf{j} + h(t) \textbf{k}.
$$

### Definition 1 - Limit of Vector

Let $\textbf{r}(t) = f(t) \textbf{i} + g(t) \textbf{j} + h(t) \textbf{k}$ be a vector function with domain $D$, and let $\textbf{L}$ be a vector. If for every number $\varepsilon > 0$, there exists a number $\delta > 0$ such that for all $t \in D$,

$$
|\mathbf{r}(t) - \mathbf{L}| < \varepsilon
\quad \text{whenever} \quad
0 < |t - t_{0}| < \delta,
$$

then

$$
\lim_{t \to t_{0}} \mathbf{r}(t) = \mathbf{L}.
$$

If $\mathbf{L} = L_{1}\mathbf{i} + L_{2}\mathbf{j} + L_{3}\mathbf{k}$, then it can be shown that $\lim_{t \to t_{0}} \mathbf{r}(t) = \mathbf{L}$ precisely when

$$
\lim_{t \to t_{0}} f(t) = L_{1}, \quad
\lim_{t \to t_{0}} g(t) = L_{2}, \quad
\lim_{t \to t_{0}} h(t) = L_{3}.
$$

### Definition 2 - Continuous of Vector

A vector function $\mathbf{r}(t)$ is **continuous at a point** $t = t_0$ in its domain if

$$
\lim_{t \to t_{0}} \mathbf{r}(t) = \mathbf{r}(t_{0}).
$$

The function is **continuous** if it is continuous at every point in its domain.

### Definition 3 - Derivative of Vector

The vector function $\textbf{r}(t) = f(t) \textbf{i} + g(t) \textbf{j} + h(t) \textbf{k}$ is **differentiable at $t$** if $f, g, h$ have derivatives at $t$. The derivative is the vector function

$$
\mathbf{r}'(t) = \frac{d\mathbf{r}}{dt}
= \lim_{\Delta t \to 0} \frac{\mathbf{r}(t + \Delta t) - \mathbf{r}(t)}{\Delta t}
= \frac{df}{dt}\mathbf{i} + \frac{dg}{dt}\mathbf{j} + \frac{dh}{dt}\mathbf{k}.
$$

### Definition 4 - Velocity and Acceleration of Vector

If $\mathbf{r}$ is the position vector of a particle moving along a smooth curve in space, then

$$
\mathbf{v}(t) = \frac{d \mathbf{r}}{dt}
$$

is the particle's **velocity vector**. If $\mathbf{v}$ is a nonzero vector, then it is tangent to the curve, and its direction is the **direction of motion**. The magnitude of $\mathbf{v}$ is the particle's **speed**, and the derivative $\mathbf{a} = \displaystyle\frac{d \mathbf{v}}{dt}$ when it exists, is the particle's **acceleration vector**.

### Vector Functions of Constant Length

If $\mathbf{r}$ is a differentiable vector function of $t$ and the length of $\mathbf{r}(t)$ is constant, then

$$
\mathbf{r} \cdot \frac{d\mathbf{r}}{dt} = 0.
$$

## 12.2 Integrals of Vector Functions; Projectile Motion

### Definition 5 - Indefinite Integral of Vector

The **indefinite integral** of $\mathbf{r}$ with respect to $t$ is $\int \mathbf{r}(t) dt$. If $\mathbf{R}$ is any antiderivative of $\mathbf{r}$, then

$$
\int \mathbf{r}(t) \ dt = \mathbf{R}(t) + C.
$$

### Definition 6 - Definite Integral of Vector

If the components $\textbf{r}(t) = f(t) \textbf{i} + g(t) \textbf{j} + h(t) \textbf{k}$ are integrable over $[a, b]$, then so is $\mathbf{r}$, and the **definite integral** of $\mathbf{r}$ from $a$ to $b$ is

$$
\int_{a}^{b} \mathbf{r}(t) \ dt =
\left(\int_{a}^{b} f(t) \ dt\right)\mathbf{i} +
\left(\int_{a}^{b} g(t) \ dt\right)\mathbf{j} +
\left(\int_{a}^{b} h(t) \ dt\right)\mathbf{k}.
$$
