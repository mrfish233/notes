## 9.1 Sequences

### Definition 1 - Convergence and Divergence

The sequence $\{a_n\}$ **converges** to the number $L$ if for every positive number $\varepsilon$ there corresponds an integer $N$ such that

$$
| a_{n} - L | < \varepsilon \qquad \text{whenever} \qquad n > N
$$

If no such number $L$ exists, we say that $\{a_{n}\}$ **diverges**. If $\{a_{n}\}$ converges to $L$, we write $\lim_{n \to \infty} a_{n} = L$, or simply $a_{n} \to L$, and call $L$ the **limit** of the sequence.

### Definition 2

The sequence $\{a_{n}\}$ **converges to infinity** if for every number $M$ there is an integer $N$ such that for all $n$ larger than $N$, $a_{n} > M$. If this condition holds, we write

$$
\lim_{n \to \infty} a_{n} = \infty \qquad
\text{or} \qquad
a_{n} \to \infty.
$$

Similarly, if for every number $m$ there is an integer $N$ such that for all $n > N$, we have $a_n < m$, then we say $\{a_n\}$ **converges to negative infinity** and write

$$
\lim_{n \to \infty} a_{n} = -\infty \qquad
\text{or} \qquad
a_n \to -\infty.
$$

### Theorem 1

Let $\{a_{n}\}$ and $\{b_{n}\}$ be sequences of real numbers, and let $A$ and $B$ be real numbers. The following rules hold if $\lim_{n \to \infty} a_{n} = A$ and $\lim_{n \to \infty} b_{n} = B$.

$$
\begin{align}
\text{Sum/Difference rule:} \qquad \qquad & \lim_{n \to \infty} (a_{n} \pm b_{n}) = A \pm B \\
\text{Constant Multiple rule:} \qquad \qquad & \lim_{n \to \infty} (k \cdot a_{n}) = k \cdot A \\
\text{Product rule:} \qquad \qquad & \lim_{n \to \infty} (a_{n} \cdot b_{n}) = A \cdot B \\
\text{Quotient rule:} \qquad \qquad & \lim_{n \to \infty} \frac{a_{n}}{b_{n}} = \frac{A}{B} \quad \text{if} \ B \ne 0 \\
\end{align}
$$

### Theorem 2 - The Sandwich Theorem

Let $\{a_{n}\}$, $\{b_{n}\}$, and $\{c_{n}\}$ be sequences of real numbers. If $a_{n} \le b_{n} \le c_{n}$ holds for all $n$ beyond some index $N$, and if

$$
\lim_{n \to \infty}a_{n}=\lim_{n \to \infty}c_{n}=L,
$$

then

$$
\lim_{n \to \infty} b_{n}=L.
$$

### Theorem 3 - The Continuous Function Theorem

Let $\{a_{n}\}$ be a sequence of real numbers. If $a_{n} \to L$ and if $f$ is a function that is continuous at $L$ and defined at all $a_{n}$, then $f(a_{n}) \to f(L)$.

### Theorem 4

Suppose that $f(x)$ is a function defined for all $x \ge n_{0}$ and that $\{a_{n}\}$ is a sequence of real number such that $a_{n}=f_{n}$ for  $n \ge n_{0}$. Then

$$
\lim_{n \to \infty}a_{n}=L \qquad \text{whenever} \qquad \lim_{x \to \infty}f(x)=L
$$

This theorem formalizes the connection between $\lim_{n \to \infty}a_{n}$ and $\lim_{x \to \infty}f(x)$.  It enables us to use *l'Hôpital's Rule* to find the limits of some sequences.

### Theorem 5

The following six sequences converge to the limits listed below.

$$
\begin{alignat}{2}
& \text{1.} \quad && \lim_{n \to \infty} \frac{\ln{n}}{n} &&= 0 &&\\
& \text{2.} \quad && \lim_{n \to \infty} \sqrt[n]{n} &&= 1 &&\\
& \text{3.} \quad && \lim_{n \to \infty} x^{\frac{1}{n}} &&= 1 &&\quad (x > 0) \\
& \text{4.} \quad && \lim_{n \to \infty} x^{n} &&= 0 &&\quad (|x| < 1) \\
& \text{5.} \quad && \lim_{n \to \infty} \left(1+\frac{x}{n}\right)^{n} &&= e^{x} &&\quad (\text{any }x) \\
& \text{6.} \quad && \lim_{n \to \infty} \frac{x^{n}}{n!} &&= 0 &&\quad (\text{any }x) \\
\end{alignat}
$$

In formulas $(3)$ through $(6)$, $x$ remains fixed as $n \to \infty$.

### Definition 3 - Bounded Monotonic Sequences

A sequence $\{a_{n}\}$ is **bounded from above** if there exists a number $M$ such that $a_{n} \le M$ for all $n$. The number $M$ is an **upper bound** of $\{a_{n}\}$. If no number less than $M$ is an upper bound for $M$, then $M$ is **least upper bound** for $\{a_{n}\}$.

A sequence $\{a_{n}\}$ is **bounded from below** if there exists a number $m$ such that $a_{n} \ge m$ for all $n$. The number $m$ is an **lower bound** of $\{a_{n}\}$. If no number less than $m$ is an upper bound for $m$, then $m$ is **greatest lower bound** for $\{a_{n}\}$.

If $\{a_{n}\}$ is bounded from *above* and *below*, then $\{a_{n}\}$ is **bounded**. If $\{a_{n}\}$ is not bounded, then $\{a_{n}\}$ is an **unbounded** sequence.

### Definition 4

A sequence $\{a_{n}\}$ is **nondecreasing** if $a_{n} \le a_{n+1}$ for all $n$. The sequence is **nonincreasing** if $a_{n} \ge a_{n+1}$ for all $n$. The sequence $\{a_{n}\}$ is **monotonic** if it is either nondecreasing or nonincreasing.

### Theorem 6 - The Monotonic Sequence Theorem

If a sequence $\{a_{n}\}$ is both *[[#Definition 3 - Bounded Monotonic Sequences|bounded]]* and *[[#Definition 4|monotonic]]*, then the sequence converges.

## 9.2 Infinite Series

### Definition 5 - Infinite Series

Given a sequence of numbers $\{a_{n}\}$, an expression of the form

$$
a_{1} + a_{2} + a_{3} + \cdots + a_{n} + \cdots
$$

is an **infinite series**. The number $a_{n}$ is the *nth term* of the series. The sequence $\{s_{n}\}$ defined by

$$
\begin{align}
s_{1} &= a_{1} \\
s_{2} &= a_{1} + a_{2} \\
s_{3} &= a_{1} + a_{2} + a_{3} \\
& \ \ \vdots \\
s_{n} &= a_{1} + a_{2} + a_{3} + \cdots + a_{n} + \cdots
= \sum\limits_{k=1}^{n} a_{k} \\
& \ \ \vdots \\
\end{align}
$$

is the **sequence of partial sum** of the series, the number $s_{n}$ being the *nth partial sum*. If the sequence of partial sums converges to a limit $L$, we say that the series **converges** and that its **sum** is $L$. In this case, we write

$$
s_{n} = a_{1} + a_{2} + a_{3} + \cdots + a_{n} + \cdots
= \sum\limits_{k=1}^{n} a_{k}
= L
$$

If the sequence of partial sums of the series does not converge, we say that the series **diverges**.

### Geometric Series

Geometric series are series of the form

$$
a + ar + ar^{2} + \cdots + ar^{n-1} + \cdots = \sum\limits_{n=1}^{\infty} ar^{n-1},
$$

in which $a$ and $r$ are fixed real numbers and $a \ne 0$. Can be written as $\sum_{n=0}^{\infty} ar^{n}$.

If $|r| < 1$, the geometric series $a + ar + ar^{2} + \cdots + ar^{n-1} + \cdots$ **converges** to $\frac{a}{1-r}$:

$$
\sum\limits_{n=1}^{\infty} ar^{n-1} = \frac{a}{1-r}
$$

If $|r| \ge 1$, the series **diverges**.

### Theorem 7 - $n$th-Term Test

If $\sum\limits_{n=1}^{\infty}a_{n}$ converges, then $a_{n} \to 0$.

### The $n$th-Term Test for Divergence

$\sum\limits_{n=1}^{\infty}a_{n}$ **diverges** if $\lim_{n \to \infty}a_{n}$ fails to exist or is different from zero. (A [[1 The Foundations - Logic and Proofs#Proofs by Contraposition|Contraposition]] of [[#Theorem 7]].)

**Example:** $\sum\limits_{n=1}^{\infty} \frac{n+1}{n}$ diverges because $\frac{n+1}{n} \to 1$.

### Theorem 8 - Combining Series

If $\sum\limits a_{n}=A$ and $\sum\limits b_{n}=B$ are convergent series, then

1. Sum/Difference Rule: $\sum\limits (a_{n} \pm b_{n})= A \pm B$
2. Constant Multiple Rule: $\sum\limits ka_{n}=kA$

## 9.3 The Integral Test

### Corollary of [[#Theorem 6 - The Monotonic Sequence Theorem|Theorem 6]]

A series $\sum\limits_{n=1}^{\infty} a_n$ of nonnegative terms **converges** if and only if its partial sums are **[[#Definition 3 - Bounded Monotonic Sequences|bounded from above]]**.

#### Example: harmonic series

The **harmonic series**

$$
\sum\limits_{n=1}^{\infty} \frac{1}{n} =
\frac{1}{1} + \frac{1}{2} + \frac{1}{3} + \cdots + \frac{1}{n} + \cdots
$$

Although $a_{n} \to 0$, the series **diverges** because there is no [[#Definition 3 - Bounded Monotonic Sequences|upper bound]] for its partial sums. By grouping the series in the following way:

$$
\begin{align}
& \frac{1}{1} + \frac{1}{2} + \frac{1}{3} + \cdots + \frac{1}{n} + \cdots \\
= & \ 1 + \left(\frac{1}{2}\right) + \left(\frac{1}{3} + \frac{1}{4}\right) + \left(\frac{1}{5} + \frac{1}{6} + \frac{1}{7} + \frac{1}{8}\right) + \cdots \\
> & \ 1 + \frac{1}{2} + \left(\frac{1}{4} + \frac{1}{4}\right) + \left(\frac{1}{8} + \frac{1}{8} + \frac{1}{8} + \frac{1}{8}\right) + \cdots \\
= & \ 1 + \frac{1}{2} + \frac{1}{2} + \frac{1}{2} + \cdots
\end{align}
$$

In general, the sum of $2^{m}$ terms ending with $\frac{1}{2^{m+1}}$ is greater than $\frac{2^{m}}{2^{m+1}} = \frac{1}{2}$. If $n = 2^k$, the partial sum $s_{n}$ is greater than $\frac{k}{2}$, so the sequence of partial sums is not bounded from above. The harmonic series **diverges**.

### Theorem 9 - The Integral Test

Let $\{a_{n}\}$ be a sequence of positive terms. Suppose that $a_{n} = f(n)$, where $f$ is a *continuous, positive, decreasing* function of $x$ for all $x \ge N$ ($N$ a positive integer). Then the series $\sum\limits_{n=N}^{\infty} a_n$ and the integral $\displaystyle\int_{N}^{\infty} f(x) \ dx$ both **converge** or both **diverge**.

- [ ] proof of the Integral Test

#### Example: $p$-series

Show that the **$p$-series**

$$
\sum\limits_{n=1}^{\infty} \frac{1}{n^{p}} =
\frac{1}{1^{p}} + \frac{1}{2^{p}} + \frac{1}{3^{p}} + \cdots + \frac{1}{n^{p}} + \cdots
$$

($p$ a real constant) converges if $p > 1$ and diverges if $p \le 1$.

**Solution:**

If $p \le 0$, the series **diverges** by the [[#The $n$th-Term Test for Divergence|nth-term test]]. 

If $0 < p < 1$, then $1-p > 0$ and

$$
\int_{1}^{\infty} \frac{1}{x^{p}} \ dx= \frac{1}{1-p} \lim_{b \to \infty} (b^{1-p} - 1) = \infty. 
$$

Therefore, the series **diverges** by [[#Theorem 9 - The Integral Test|the Integral Test]].

If $p = 1$, it is [[#Example harmonic series|harmonic series]] which **diverges**.

If $p > 1$, then $f(x) = \frac{1}{x^{p}}$ is a positive, continuous and decreasing function of $x$. Since

$$
\begin{align}
\int_{1}^{\infty} \frac{1}{x^{p}} \ dx &=
\int_{1}^{\infty} x^{-p} \ dx = \lim_{b \to \infty} \left[\frac{x^{-p+1}}{-p+1}\right]_{1}^{b} \\
&= \frac{1}{1-p} \lim_{b \to \infty} \left(\frac{1}{b^{p-1}} - 1\right) \\
&= \frac{1}{1-p} (0-1) \\
&= \frac{1}{p-1}.
\end{align}
$$

The series **converges** by [[#Theorem 9 - The Integral Test|the Integral Test]].

## 9.4 Comparison Tests

### Theorem 10 - Direct Comparison Test

Let $\sum\limits{a_n}$ and $\sum\limits{b_n}$ be two series with $0 \le a_{n} \le b_{n}$ for all $n$. Then

1. If $\sum\limits{b_n}$ **converges**, then $\sum\limits{a_n}$ also **converges**.
2. If $\sum\limits{a_n}$ **diverges**, then $\sum\limits{b_n}$ also **diverges**.

**Example:** The series

$$
\sum\limits_{n=0}^{\infty} \frac{1}{n!} = 1 + \frac{1}{1!} + \frac{1}{2!} + \frac{1}{3!} + \cdots
$$

converges as its terms are all positive and less than corresponding terms of

$$
1 + \sum\limits_{n=0}^{\infty} \frac{1}{2^{n}} = 1 + 1 + \frac{1}{2} + \frac{1}{2^{2}} + \cdots
$$

The [[#Geometric Series|geometric series]] converges and we have

$$
1 + \sum\limits_{n=0}^{\infty} \frac{1}{2^{n}} = 1 + \frac{1}{1-(\frac{1}{2})} = 3
$$

### Theorem 11 - The Limit Comparison Test

Suppose that $a_{n} > 0$ and $b_{n} > 0$ for all $n \ge N$ ($N$ an integer).

1. If $\displaystyle\lim_{n \to \infty} \frac{a_{n}}{b_{n}} = c$ and $c > 0$, then $\sum\limits a_{n}$ and $\sum\limits b_{n}$ both **converge** or **diverge**.
2. If $\displaystyle\lim_{n \to \infty} \frac{a_{n}}{b_{n}} = 0$ and $\sum\limits b_{n}$ **converges**, then $\sum\limits a_{n}$ **converges**.
3. If $\displaystyle\lim_{n \to \infty} \frac{a_{n}}{b_{n}} = \infty$ and $\sum\limits b_{n}$ **diverges**, then $\sum\limits a_{n}$ **diverges**.

**Example:** $\sum\limits_{n = 2}^{\infty} \frac{1 + n \ln{n}}{n^{2}+5}$

Let $a_{n} = \frac{1 + n \ln{n}}{n^{2}+5}$ and $b_{n} = \frac{1}{n}$, $a_{n}$ and $b_{n}$ are positive for each $n$, and

$$
\sum\limits_{n=2}^{\infty} b_{n} = \sum\limits_{n=2}^{\infty} \frac{1}{n} \ \text{diverges,}
$$

and

$$
\lim_{n \to \infty} \frac{a_{n}}{b_{n}} = \lim_{n \to \infty} \frac{n + n^{2} \ln n}{n^{2}+ 5} = \infty,
$$

therefore $\sum\limits a_{n}$ diverges.

## 9.5 Absolute Convergence; The Ratio and Root Tests

### Definition 6 - Absolute Convergence

A series $\sum\limits a_{n}$ **converges absolutely** (is **absolutely convergent**) if the corresponding series of absolute values, $\sum\limits |a_{n}|$, converges.

### Theorem 12 - The Absolute Convergence Test

If $\sum\limits_{n=1}^{\infty} |a_{n}|$ **converges**, then $\sum\limits_{n=1}^{\infty} a_{n}$ **converges**.

**Proof:** for each $n$, 

$$
-|a_{n}|  \le a_{n} \le |a_{n}|, \qquad \text{so} \qquad 0 \le a_{n} + |a_{n}| \le 2|a_{n}|
$$

If $\sum\limits_{n=1}^{\infty} |a_{n}|$ converges, then $\sum\limits_{n=1}^{\infty} 2|a_{n}|$ converges, and by [[#Theorem 10 - Direct Comparison Test| Direct Comparison Test]], the nonnegative series $\sum\limits_{n=1}^{\infty} (a_{n} + |a_{n}|)$ converges. Then

$$
\begin{align}
\sum\limits_{n=1}^{\infty} a_{n}
&= \sum\limits_{n=1}^{\infty} (a_{n} + |a_{n}| - |a_{n}|) \\
&= \sum\limits_{n=1}^{\infty} (a_{n} + |a_{n}|) - \sum\limits_{n=1}^{\infty} |a_{n}|.
\end{align}
$$

Therefore $\sum\limits_{n=1}^{\infty} a_{n}$ **converges**.

### Theorem 13 - The Ratio Test

Let $\sum\limits a_{n}$ be any series and suppose that

$$
\lim_{n \to \infty} \left|\frac{a_{n+1}}{a_{n}}\right| = \rho.
$$

Then

1. The series *converges absolutely* if $\rho < 1$
2. The series *diverges* if $\rho > 1$ or $\rho$ is infinite
3. The test is inconclusive if $\rho = 1$.

**Proof:**

- [ ] proof of The Ratio Test

### Theorem 14 - The Root Test

Let $\sum\limits a_{n}$ be any series and suppose that

$$
\lim_{n \to \infty} \sqrt[n]{|a_{n}|} = \rho
$$

Then

1. The series *converges absolutely* if $\rho < 1$
2. The series *diverges* if $\rho > 1$ or $\rho$ is infinite
3. The test is inconclusive if $\rho = 1$.

**Proof: **

- [ ] proof of The Root Test

**Example:** the series $a_{n}$ with terms

$$
a_{n} = 
\begin{cases}
\frac{n}{2^{n}}, \quad & n \text{ odd} \\
\frac{1}{2^{n}}, \quad & n \text{ even}.
\end{cases}
$$

By applying the Root Test, we have

$$
\sqrt[n]{|a_{n}|} = 
\begin{cases}
\frac{\sqrt[n]{n}}{2}, \quad & n \text{ odd} \\
\frac{1}{2}, \quad & n \text{ even}.
\end{cases}
$$

Therefore

$$
\frac{1}{2} \le \sqrt[n]{a_{n}} \le \frac{\sqrt[n]{n}}{2}
$$

Since $\sqrt[n]{n} \to 1$ ([[#Theorem 5]]), we have $\sqrt[n]{a_{n}} \to \frac{1}{2}$ by the [[#Theorem 2 - The Sandwich Theorem|Sandwich Theorem]]. As the limit is less than 1, so the series converges by the Root Test.

## 9.6 Alternating Series and Conditional Convergence

An **alternating series** is a series in which the terms are alternately positive and negative. For example:

$$
1 - \frac{1}{2} + \frac{1}{3} - \frac{1}{4} + \cdots + \frac{(-1)^{n+1}}{n} + \cdots
$$

The $n$th term of an alternating series is of the form

$$
a_{n} = (-1)^{n+1} u_{n} \qquad \text{or} \qquad a_{n} = (-1)^{n} u_{n}
$$

### Theorem 15 - The Alternating Series Test

The series

$$
\sum\limits_{n=1}^{\infty} (-1)^{n+1} u_{n} = u_{1} - u_{2} + u_{3} - u_{4} + \cdots
$$

**converges** if the following conditions are satisfied:

1. The $u_{n}$'s are all positive
2. The $u_{n}$'s are eventually nonincreasing: $u_{n}\ge u_{n+1}$ for all $n \ge N$, for some integer $N$.
3. $u_{n} \to 0$

**Proof:** 

- [ ] proof of Alternating Series Test

### Definition 7 - Conditional Convergence

A series that is **convergent** but not [[#Definition 6 - Absolute Convergence|absolutely convergent]] is called **conditionally convergent**.

### Theorem 17 - The Rearrangement Theorem for Absolutely Convergent Series

If $\sum\limits_{n=1}^{\infty}$ converges absolutely, and $b_{1}, b_{2}, b_{3}, \cdots, b_{n}, \cdots$ is any arrangement of the sequence $\{a_{n}\}$, then $\sum\limits b_{n}$ converges absolutely and

$$
\sum\limits_{n=1}^{\infty} b_{n} = \sum\limits_{n=1}^{\infty} a_{n}
$$

### Summary of Tests

1. **[[#The $n$th-Term Test for Divergence|The nth-term test for divergence]]**: Unless $a_{n}\to 0$, the series **diverges**.
2. **[[#Geometric Series]]**: $\sum\limits ar^{n}$ **converges** if $|r| < 1$; otherwise, it **diverges**.
3. **[[#Example $p$-series|p-series]]**: $\sum\limits \frac{1}{n^{p}}$ **converges** if $p > 1$; otherwise, it **diverges**.
4. **Series with nonnegative terms**: Try the [[#Theorem 9 - The Integral Test|Integral Test]] or try comparing to a known series with the [[#Theorem 10 - Direct Comparison Test|Direct Comparison Test]] or the [[#Theorem 11 - The Limit Comparison Test|Limit Comparison Test]]. Try the [[#Theorem 13 - The Ratio Test|Ratio Test]] or [[#Theorem 14 - The Root Test|Root Test]].
5. **Series with some negative terms**: Check if the series $\sum\limits |a_{n}|$ converges by the tests listed above, as the [[#Theorem 12 - The Absolute Convergence Test|Absolute Convergence Test]] implies convergence.
6. **Alternating series**: $\sum\limits a_{n}$ **converges** if the series satisfies the conditions of the [[#Theorem 15 - The Alternating Series Test|Alternating Series Test]].

## 9.7 Power Series

### Definition 8 - Power Series

A power series about $x = 0$ is a series of the form

$$
\sum\limits_{n=0}^{\infty} c_{n} x^{n} = 
c_{0} + c_{1}x + c_{2}x^{2} + \cdots + c_{n}x^{n} + \cdots.
$$

A power series about $x = a$ is a series of the form

$$
\sum\limits_{n=0}^{\infty} c_{n} (x-a)^{n} = 
c_{0} + c_{1}(x-a) + c_{2}(x-a)^{2} + \cdots + c_{n}(x-a)^{n} + \cdots
$$

in which the **center** $a$ and the **coefficients** $c_{0}, c_{1}, c_{2}, \cdots, c_{n}, \cdots$ are constants.

**Example:**

The power series

$$
1 - \frac{1}{2} (x-2) + \frac{1}{4} (x-2)^{2} + \cdots + \left(-\frac{1}{2}\right)^{n-1} (x-2)^{n} + \cdots
$$

has first term $1$ and ratio $r = \displaystyle-\frac{x-2}{2}$. The series converges for

$$
\begin{align}
|r| &< 1 \\
\left|\frac{x-2}{2}\right| &< 1 \\
\end{align}
$$

which simplifies to $0 < x < 4$. The sum is

$$
\frac{1}{1-r} = \frac{1}{1+\frac{x-2}{2}} = \frac{2}{x}.
$$

### Theorem 18 - The Convergence Theorem for Power Series

If the power series

$$
\sum\limits_{n=0}^{\infty} a_{n}x^{n} = a_{0} + a_{1}x + a_{2}x^{2} + \cdots
$$

converges at $x = c \ne 0$, then it **converges absolutely** for all $x$ with $|x| < |c|$. If the series diverges at $x = d$, then it **diverges** for all $x$ with $|x| > |d|$.

**Proof:**

- [ ] proof of Theorem 18

### Corollary of [[#Theorem 18 - The Convergence Theorem for Power Series|Theorem 18]]

The convergence of the series $\sum\limits c_{n}(x-a)^{n}$ is described by one of the following 3 cases.

1. There is a positive number $R$ such that the series diverges for $x$ with $|x-a| > R$ but **converges absolutely** for $x$ with $|x-a| < R$. The series may or may not converge at either of the endpoints $x = a-R$ and $x = a + R$.
2. The series **converges absolutely** for every $x \ (R = \infty)$.
3. The series **converges** at $x = a$ and **diverges** elsewhere $(R = 0)$.

$R$ is called the **radius of convergence** of the power series, and the interval or radius $R$ centered at $x=a$ is called the **interval of convergence**.

- [ ] proof of Corollary of Theorem 18

### Tests of Convergence of Power Series

1. Use the **Ratio Test or Root Test** to find the largest open interval where the series converges absolutely.

$$
|x-a| < R
$$

2. If $R$ is finite, test for convergence or divergence at endpoint.
3. If $R$ is finite, the series **diverges** for $|x-a| > R$ as the $n$th term does not approach zero for those values of $x$.

### Theorem 19 - Series Multiplication for Power Series

If $A(x) = \sum\limits_{n=0}^{\infty} a_{n}x^{n}$ and $B(x) = \sum\limits_{n=0}^{\infty} b_{n}x^{n}$ **converge absolutely** for $|x| < R$, and

$$
c_{n} = a_{0}b_{n} + a_{1}b_{n-1} + a_{2}b_{n-2} + \cdots + a_{n-1}b_{1} + a_{n}b_{0} = \sum\limits_{k=0}^{n} a_{k}b_{n-k},
$$

then $\sum\limits_{n=0}^{\infty} c_{n}x^{n}$ **converges absolutely** to $A(x)B(x)$ for $|x| < R$:

$$
\left(\sum\limits_{n=0}^{\infty} a_{n}x^{n}\right)
\left(\sum\limits_{n=0}^{\infty} b_{n}x^{n}\right)
= \sum\limits_{n=0}^{\infty} c_{n}x^{n}
$$

### Theorem 20

If $\sum\limits_{n=0}^{\infty} a_{n}x^{n}$ **converges absolutely** for $|x| < R$, and $f$ is a continuous function, then $\sum\limits_{n=0}^{\infty} a_{n}f(x^{n})$ **converges absolutely** on the set of points $x$, where $|f(x)| < R$.

### Theorem 21 - Term-by-Term Differentiation

If $\sum\limits c_{n}(x-a)^{n}$ has radius of convergence $R > 0$, it defines a function

$$
f(x) = \sum\limits_{n=0}^{\infty} c_{n}(x-a)^{n} \quad \text{on the interval} \quad |x-a| < R.
$$

This function $f$ has derivatives of all orders inside the interval, obtain the derivatives by differentiating the original series term by term:

$$
\begin{align}
f'(x) &= \sum\limits_{n=0}^{\infty} nc_{n}(x-a)^{n-1}, \\
f''(x) &= \sum\limits_{n=0}^{\infty} n(n-1)c_{n}(x-a)^{n-2},
\end{align}
$$

and so on. Each of these derived series **converges** at every point of the interval
$a - R < x < a + R$.

### Theorem 22 - Term-by-Term Integration

Suppose that

$$
f(x) = \sum\limits_{n=0}^{\infty} c_{n}(x-a)^{n}
$$

**converges** for $a - R < x < a + R$ (where $R > 0$). Then

$$
\int f(x) \ dx = \sum\limits_{n=0}^{\infty} c_{n} \frac{(x-a)^{n-1}}{n+1} + C
$$

**converges** for $a - R < x < a + R$.

## 9.8 Taylor and Maclaurin Series

### Definition 9 - Taylor and Maclaurin Series

Let $f$ be a function with derivatives of all orders throughout some interval containing $a$ as an interior point. Then the **Taylor series** generated by $f$ at $x = a$ is

$$
\begin{align}
\sum\limits_{k=0}^{\infty} \frac{f^{(k)}(a)}{k!} (x-a)^{k} = f(a) &+ f'(a)(x-a) + \frac{f''(a)}{2!} (x-a)^{2} \\
&+ \cdots + \frac{f^{(n)}(a)}{n!} (x-a)^{n} + \cdots.
\end{align}
$$

The **Maclaurin series** of $f$ is the Taylor series generated by $f$ at $x=0$, or

$$
\sum\limits_{k=0}^{\infty} \frac{f^{(k)}(0)}{k!} x^{k} = f(0) + f'(0)x + \frac{f''(0)}{2!} x^{2} + \cdots + \frac{f^{(n)}(0)}{n!} x^{n} + \cdots.
$$

### Definition 10 - Taylor Polynomial

Let $f$ be a function with derivatives of order $k$ for $k = 1, 2, \cdots, N$ in some interval containing $a$ as an interior point. Then the **Taylor polynomial of order $n$** generated by $f$ at $x=a$ is the polynomial

$$
P_{n}(x) = f(a) + f'(a)(x-a) + \frac{f''(a)}{2!} (x-a)^{2} + \cdots + \frac{f^{(n)}(a)}{n!} (x-a)^{n}.
$$

**Example 1:**

The Taylor series and Taylor polynomials of $f(x) = e^{x}$ at $x = 0$ has $f^{(n)}(x) = e^x$ and $f^{(n)}(0) = 1$ for every $n$, then

$$
\begin{align}
e^{x} &= f(0) + f'(0)x + \frac{f''(0)}{2!}x^{2} + \cdots + \frac{f^{(n)}(0)}{n!}x^{n} + \cdots \\
&= 1 + x + \frac{x^{2}}{2!} + \cdots + \frac{x^{n}}{n!} + \cdots \\
&= \sum\limits_{k=0}^{\infty} \frac{x^{k}}{k!}.
\end{align}
$$

## 9.9 Convergence of Taylor Series

### Theorem 23 - Taylor's Theorem

If $f$ and its first $n$ derivatives $f', f'', \cdots, f^{(n)}$ are continuous on $[a,b]$, and $f^{(n)}$ is differentiable on $(a, b)$, then there exists a number $c, a < c < b$ such that

$$
\begin{align}
f(b) = f(a) &+ f'(a)(b-a) + \frac{f''(a)}{2!} (b-a)^{2} + \cdots \\
&+ \frac{f^{(n)}(a)}{n!} (b-a)^{n} + \frac{f^{(n+1)}(a)}{(n+1)!} (b-a)^{n+1}
\end{align}
$$

### Taylor's Formula

(Taylor's formula is easier to use in circumstances by changing $b$ to $x$.)

If $f$ has derivatives of all orders in an open interval $I$ containing $a$, then $\forall n$ and $\forall x \in I$,

$$
\begin{align}
f(x) = f(a) &+ f'(a)(x-a) + \frac{f''(a)}{2!} (x-a)^{2} + \cdots \\
&+ \frac{f^{(n)}(a)}{n!} (x-a)^{n} + R_{n}(x)
\end{align}
$$

where

$$
R_{n}(x) = \frac{f^{n+1}(c)}{n!}(x-a)^{(n+1)!} (x-a)^{n+1}
$$

for some $c$ between $a$ and $x$.

If $R_{n(x)}\to 0$ as $n \to \infty, \forall x \in I$, then the Taylor series generated by $f$ at $x=a$ **converges** to $f$ on $I$, and we write

$$
f(x) = \sum\limits_{k=0}^{\infty} \frac{f^{(k)}(a)}{k!} (x-a)^{k}.
$$

### Theorem 24 - The Remainder Estimation Theorem

If there exists $M > 0$ such that $|f^{(n+1)}(t)| \le M$ for all $t$ between $x$ and $a$, inclusive, then the remainder term $R_{n}(x)$ in Taylor's Theorem satisfies the inequality

$$
|R_{n}(x)| \le M \frac{|x-a|^{(n+1)}}{(n+1)!}.
$$

If this inequality holds for every $n$, and the other conditions of Taylor's Theorem are satisfied by $f$, then the series **converges** to $f(x)$.
