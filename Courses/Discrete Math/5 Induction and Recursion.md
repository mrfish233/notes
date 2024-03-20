# 5 Induction and Recursion

## 5.1 Mathematical Induction

### Principle of Mathematical Induction

To prove that $P(n)$ is true for all positive integers $n$, where $P(n)$ is a propositional function, we complete 2 steps:

1. **Basis Step**: We verify that $P(1)$ is true.
2. **Inductive Step**: We show that the conditional statement $P(k) \to P(k+1)$ is *true* for all positive integers $k$.

When the domain is the set of positive integers, it can be stated as

$$
(P(1) \land \forall k (P(k) \to P(k+1))) \to \forall n P(n).
$$

## 5.2 Strong Induction and Well-Ordering

### Strong Induction

Strong induction differs from mathematical induction is that the inductive step shows that if $P(j)$ is true for $j = 1, 2, 3, \cdots, k$, then $P(k+1)$ is true.

1. **Basis Step**: We verify that $P(1)$ is true.
2. **Inductive Step**: We show that the conditional statement $[P(1) \land P(2) \land P(3) \land \cdots \land P(k)] \to P(k+1)$ is *true* for all positive integers $k$.

### The Well-Ordering Property

Every nonempty set of nonnegative integers has a **least** element.

## 5.3 Recursive Definitions and Structural Introduction

### Example of Fibonacci Sequence

Let $f(n)$ be the $n$th Fibonacci number. Then

$$
\forall n \ge 3, f(n) > \alpha^{n-2},
\quad \text{where} \quad
\alpha = \frac{1+\sqrt{5}}{2}.
$$

**Proof:**

*Basis Step*: we have

$$
\begin{align}
f(3) &= 2 > \left(\frac{1+\sqrt{5}}{2}\right)^{3-2} \\
f(4) &= 3 > \left(\frac{1+\sqrt{5}}{2}\right)^{4-2} = \frac{3+\sqrt{5}}{2}
\end{align}
$$

therefore $f(3)$ and $f(4)$ are true.

*Inductive Step*: Assume $f(j)$ is true, where $j = 3, 4, \cdots, k \ (k \ge 4)$. We must show that $f(k+1) > \alpha^{k-1}$ is true. Then

$$
\begin{align}
f(k+1) &= f(k) + f(k-1) \\
&> \alpha^{k-2} + \alpha^{k-3} \\
&= \alpha^{k-3} (\alpha + 1) \\
&= \alpha^{k-3} \alpha^{2} \\
&= \alpha^{k-1}.
\end{align}
$$

This complete the proof.

### Theorem 1 - Lamé's Theorem

Let $a$ and $b$ be positive integers with $a \ge b$. Let $n$ be the number of divisions used by [the Euclidean Algorithm](4%20Number%20Theory%20and%20Cryptography.md#The%20Euclidean%20Algorithm) to find $\gcd (a, b)$, then $n$ is at most $5$ times the number of decimal digits of $b$.

**Proof:**

When the Euclidean algorithm is applied to find $\gcd (a, b)$ with $a \ge b$, this sequence of equations is obtained:

$$
\begin{align}
a = r_{0} &= r_{1}k_{1} + r_{2} \\
b = r_{1} &= r_{2}k_{2} + r_{3} \\
&\ \ \vdots \\
r_{n-2} &= r_{n-1}k_{n-1} + r_{n} \\
r_{n-1} &= r_{n}k_{n} + 0
\end{align}
$$

The quotients $k_{1}, k_{2}, k_{3}, \cdots, k_{n-1} \ge 1$ and $k_{n} \ge 2$ since $0 \le r_{n} < r_{n-1}$. This implies that

$$
\begin{align}
r_{n} &\ge 1 &&= f_{2} \\
r_{n-1} &\ge 2r_{n} \ge 2f_{2} &&= f_{3} \\
r_{n-2} &\ge r_{n-1} + r_{n} \ge f_{3} + f_{2} &&= f_{4} \\
r_{n-3} &\ge r_{n-2} + r_{n-1} \ge f_{4} + f_{3} &&= f_{5} \\
& \ \ \vdots \\
r_{2} &\ge r_{3} + r_{4} \ge f_{n-1} + f_{n-2} &&= f_{n} \\
b = r_{1} &\ge r_{2} + r_{3} \ge f_{n} + f_{n-1} &&= f_{n+1} 
\end{align}
$$

This shows that $b \ge f_{n+1}$. From [previous example](#Example%20of%20Fibonacci%20Sequence), we know that $f_{n+1} > \alpha^{n-1}$ for $n > 2$. Therefore

$$
\begin{align}
b &> \alpha^{n-1} \\
\log{b} &> (n-1) \log \alpha \qquad (\log \alpha \approx 0.208 > 1/5) \\
&> \frac{n-1}{5}.
\end{align}
$$

Hence we have $n-1 < 5 \log b$. Suppose that $b$ has $k$ decimal digits, then $b < 10^{k}$ and

$$
n-1 < 5 \log 10^{k} = 5k.
$$

As $k$ is an integer, it follows that $n \le 5k$. This finishes the proof.
