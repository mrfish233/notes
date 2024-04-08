# 8 Advanced Counting Techniques

## 8.2 Solving Linear Recurrence Relations

### Definition 1 - Linear Recurrence Relation

A **linear homogeneous relation** of degree $k$ with constant coefficients is a recurrence relation of the form

$$
a_{n} = c_{1} a_{n-1} + c_{2} a_{n-2} + \cdots + c_{k} a_{n-k},
$$

where $c_{1}, c_{2}, \cdots, c_{k}$ are real numbers, and $c_{k} \ne 0$.

Example:

1. $T(n) = T(n-1) + T(n-2)$ is a linear homogeneous recurrence of degree $2$.
2. $a_{n} = a_{n-1} + a_{n-2}^{2}$ is not linear
3. $b_{n} = 2b_{n} - 1$ is not homogeneous

### Theorem 1 - The Degree Two Case with Distinct Root

Let $c_{1}$ and $c_{2}$ be real numbers. Suppose that $r^{2} - c_{1}r - c_{2} = 0$ has two distinct roots $r_{1}$ and $r_{2}$, then the sequence $\{a_{n}\}$ is a solution of the relation $a_{n} = c_{1}a_{n-1} + c_{2}a_{n-2}$ **if and only if**

$$
a_{n} = \alpha_{1} r_{1}^{n} + \alpha_{2} r_{2}^{n},
\quad n = 0, 1, 2, \cdots
$$

where $\alpha_{1}, \alpha_{2}$ are constants.

**Proof:**

*(Forward Proof)*

*(Backward Proof)* Let $a_{n} = \alpha_{1} r_{1}^{n} + \alpha_{2} r_{2}^{n}$ where $n = 0, 1, 2, \cdots$ and $\alpha_{1}, \alpha_{2}$ are constants. Then we have

$$
a_{n-1} = \alpha_{1} r_{1}^{n-1} + \alpha_{2} r_{2}^{n-1}
\quad \text{and} \quad
a_{n-2} = \alpha_{1} r_{1}^{n-2} + \alpha_{2} r_{2}^{n-2}.
$$

Then

$$
\begin{align}
c_{1}a_{n-1} + c_{2}a_{n-2} &=
c_{1}(\alpha_{1} r_{1}^{n-1} + \alpha_{2} r_{2}^{n-1}) + 
c_{2}(\alpha_{1} r_{1}^{n-2} + \alpha_{2} r_{2}^{n-2}) \\
&= \alpha_{1}(c_{1} r_{1}^{n-1} + c_{2} r_{1}^{n-2}) + 
\alpha_{2}(c_{1} r_{2}^{n-1} + c_{2} r_{2}^{n-2}).
\end{align}
$$

From $r^{2} - c_{1}r - c_{2} = 0$, we know that

$$
r^{n} = c_{1} r^{n-1} + c_{2} r^{n-2},
$$

hence

$$
\begin{align}
c_{1}a_{n-1} + c_{2}a_{n-2}
&= \alpha_{1}(c_{1} r_{1}^{n-1} + c_{2} r_{1}^{n-2}) + 
\alpha_{2}(c_{1} r_{2}^{n-1} + c_{2} r_{2}^{n-2}) \\
&= \alpha_{1} r_{1}^{n} + \alpha_{2} r_{2}^{n} \\
&= a_{n}.
\end{align}
$$

Therefore this complete our proof.

### Theorem 2 - The Degree Two Case with Same Root

Let $c_{1}$ and $c_{2}$ be real numbers. Suppose that $r^{2} - c_{1}r - c_{2} = 0$ has only one root $r_{0}$, then the sequence $\{a_{n}\}$ is a solution of the relation $a_{n} = c_{1}a_{n-1} + c_{2}a_{n-2}$ **if and only if**

$$
a_{n} = \alpha_{1} r_{0}^{n} + \alpha_{2} n r_{0}^{n},
\quad n = 0, 1, 2, \cdots
$$

where $\alpha_{1}, \alpha_{2}$ are constants.

## 8.4 Generating Functions

### Definition 2 - Generating Function

The **generating function** for the sequence $a_{0}, a_{1}, a_{2}, \cdots, a_{k}, \cdots$ of real numbers is the infinite series

$$
G(x) = a_{0} + a_{1}x + a_{2}x^{2} + \cdots + a_{k}x^{k} + \cdots
= \sum\limits_{k=0}^{\infty} a_{k} x^{k}.
$$

The generating function for $\{a_{k}\}$ is sometimes called the **ordinary generating function** of $\{a_{k}\}$ to distinguish it from other types of generating functions for this sequence.

### Theorem 3 - Addition and Multiplication

Let $f(x) = \sum\limits_{k=0}^{\infty} a_{k}x^{k}$ and $g(x) = \sum\limits_{k=0}^{\infty} b_{k}x^{k}$. Then

$$
f(x) + g(x) = \sum\limits_{k=0}^{\infty} (a_{k} + b_{k})x^{k}
$$

and

$$
f(x)g(x) = \sum\limits_{k=0}^{\infty} \left( \sum\limits_{j=0}^{k} a_{j} b_{k-j} \right) x^{k}.
$$

### Definition 3 - Extended binomial coefficient

Let $u$ be a real number and $k$ a nonnegative integer. Then the **extended binomial coefficient** $\binom{u}{k}$ is defined by

$$
\binom{u}{k} =
\begin{cases}
\displaystyle\frac{u (u-1) (u-2) \cdots (u-k+1)}{k!}, &\quad k \ge 0 \\
1, &\quad k = 0.
\end{cases}
$$

### Theorem 4 - The Extended Binomial Theorem

Let $x$ be a real number with $|x| < 1$ and let $u$ be a real number. Then

$$
(1+x)^{u} = \sum\limits_{k=0}^{\infty} \binom{u}{k} x^{k}.
$$

This theorem can be proved using the theory of [Maclaurin Series](9%20Infinite%20Sequences%20and%20Series.md#Definition%209%20-%20Taylor%20and%20Maclaurin%20Series|Maclaurin%20Series).
