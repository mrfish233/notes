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
