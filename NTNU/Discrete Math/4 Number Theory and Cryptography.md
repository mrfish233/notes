## 4.1 Divisibility and Modular Arithmetic

### Definition 1 - Division

If $a$ and $b$ are integers with $a \ne 0$, we say that **$a$ divides $b$** if there is an integer $c$ such that

$$
b = ac.
$$

When $a$ divides $b$, $a$ is a **factor** or **divisor** of $b$, and that $b$ is a multiple of $a$. The notation of $a$ divides $b$ is $a \mid b$, and we write $a \not \mid b$ when $a$ does not divide $b$.

### Theorem 1

Let $a, b, c$ be integers, where $a \ne 0$. Then

$$
\begin{align}
\text{(i)} & \text{ if } a \mid b \text{ and } a \mid c, \text{ then } a \mid (b \pm c); \\
\text{(ii)} & \text{ if } a \mid b, \text{ then } a \mid bc \text{ for all integers } c; \\
\text{(iii)} & \text{ if } a \mid b \text{ and } b \mid c, \text{ then } a \mid c.
\end{align}
$$

### Theorem 2 - The Division Algorithm

Let $a$ be an integer and $d$ a positive integer. Then there are unique integers $q, r$ with $0 \le r < d$, such that

$$
a = dq + r.
$$

### Definition 2

In the [[#Theorem 2 - The Division Algorithm|Division Algorithm]], $d$ is called the **divisor**, $a$ is called the **dividend**, $q$ is called the **quotient**, and $r$ is called the **remainder**. The notation

$$
q = a \text{ div } d, \quad r = a \bmod d
$$

is used to express the quotient and remainder.

### Definition 3 - Congruence

If $a$ and $b$ are integers and $m$ is a positive integer, then $a$ is *congruent to* $b$ *modulo* $m$ if $m$ divides $a-b$, that is $m \mid (a-b)$. Its notation is

$$
a \equiv b \pmod{m}.
$$

We say that $a \equiv b \pmod{m}$ is a **congruence** and that $m$ is its **modulus**.

### Theorem 3/4 - Properties of Congruence

Let $a$ and $b$ be integers, and let $m$ be a positive integer. Then $a \equiv b \pmod{m}$ if and only if

$$
\begin{align}
\text{1. } & a \bmod m = b \bmod m; \\
\text{2. } & \text{there exists an integer } k \text{ such that } a = b + km.
\end{align}
$$

### Theorem 5 - Addition and Multiplication Rules

Let $m$ be a positive integer. If $a \equiv b \pmod{m}$ and $c \equiv d \pmod{m}$, then

$$
a + c \equiv b + d \pmod{m} \qquad \text{and} \qquad ac \equiv bd \pmod{m}
$$

**Proof:** (by [[1 The Foundations - Logic and Proofs#Direct Proofs|direct proof]])

Since $a \equiv b \pmod{m}$ and $c \equiv d \pmod{m}$, by [[#Theorem 3/4 - Properties of Congruence|Theorem 4]] there exist integers $k_{1}$ and $k_{2}$ with $b = a + k_{1}m$ and $d = c + k_{2}m$. Hence,

$$
\begin{align}
b + d &= (a + k_{1}m) + (c + k_{2}m) \\
&= (a + c) + m(k_{1} + k_{2})
\end{align}
$$

and

$$
\begin{align}
bd &= (a + k_{1}m)(c + k_{2}m) \\
&= ac + m(k_{1}c + k_{2}a + k_{1}k_{2}m).
\end{align}
$$

Therefore

$$
a + c \equiv b + d \pmod{m} \qquad \text{and} \qquad ac \equiv bd \pmod{m}.
$$

### Corollary 2

Let $m$ be a positive integer and $a$ and $b$ be integers. Then

$$
(a+b) \bmod m = ((a \bmod m) + (b \bmod m)) \bmod m
$$

and

$$
ab \bmod m = ((a \bmod m)(b \bmod m)) \bmod m.
$$

## 4.3 Primes and Greatest Common Divisors

### Definition 1 - Prime and Composite

An integer $p$ greater than $1$ is called **prime** is the only positive factors of $p$ are $1$ and $p$. A positive integer that is greater that $1$ and is not prime is called **composite**.

### Theorem - The Fundamental Theorem of Arithmetic

Every integer greater than $1$ can be written uniquely as a prime or as the product of two or more primes, where the prime factors are written in order of nondecreasing size.

**Example:**

1. $100 = 2 \cdot 2 \cdot 5 \cdot 5 = 2^{2}5^{2}$
2. $641 = 641$

### Theorem 2 - Composite Integer

If $n$ is a [[#Definition 1 - Prime and Composite|composite integer]], then $n$ has a prime divisor less than or equal to $\sqrt{n}$.

#### The Sieve of Eratosthenes

This is used to find all primes not exceeding a specified positive integer. It does so by iteratively marking as **composite** the multiples of each prime, starting with the first prime number, 2. Once all the multiples of each discovered prime have been marked as composites, the remaining unmarked numbers are primes. (from [Wikipedia](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes))

### Theorem 3 - Euclid's Theorem

There are infinitely many primes.

**Proof:** (by [[1 The Foundations - Logic and Proofs#Proofs by Contradiction| Contradiction]])

Assume $p_{1}, p_{2}, p_{3}, \cdots, p_{n}$ is a finite list of prime numbers. Let

$$
P = p_{1} p_{2} p_{3} \cdots p_{n} \quad \text{ and } \quad
Q = P + 1
$$

By the [[#Theorem - The Fundamental Theorem of Arithmetic|fundamental theorem of arithmetic]], $Q$ is prime or else it can be written as the product of two or more primes.

- If $Q$ is prime, then there is at lease one or more prime that is not in the list $p_{1}, p_{2}, p_{3}, \cdots, p_{n}$, namely, $Q$ itself.
- If $Q$ is not prime, then there exists $p_{j}$ is a prime factor of $Q$. $p_j$ can't be any of $p_{1}, p_{2}, p_{3}, \cdots, p_{n}$ since $Q$ has remainder of $1$ when divided by each $p_i$. Therefore $p$ is a prime not on our list.

Hence, there is a prime not in the list $p_{1}, p_{2}, p_{3}, \cdots, p_{n}$ in both cases above. This is a **contradiction** because we assume that we have listed all the primes. Consequently, there are infinitely many primes.

### Theorem 4 - The Prime Number Theorem

The ratio of $\pi{(x)}$ (the number of primes not exceeding $x$) and $\displaystyle\frac{x}{\ln x}$ approaches $1$ as $x$ grows without bound.

### Definition 2 - Greatest Common Divisor

Let $a$ and $b$ be integers, not both zero. The largest integer $d$ such that $d \mid a$ and $d \mid b$ is called the **greatest common divisor** of $a$ and $b$. The notation is

$$
d = \gcd (a,b)
$$

#### The Euclidean Algorithm

This algorithm is an efficient method of finding the greatest common divisor.

**Example:** $\gcd (91, 287)$

$$
\begin{align}
\textcolor{#e64553}{287} &= \textcolor{#fe640b}{91} \cdot 3 + \textcolor{#df8e1d}{14} \\
\textcolor{#fe640b}{91} &= \textcolor{#df8e1d}{14} \cdot 6 + \textcolor{#40a02b}{7} \\
\textcolor{#df8e1d}{14} &= \textcolor{#40a02b}{7} \cdot 2 + 0
\end{align}
$$

### Definition 3/4 - Relatively Prime

The integers $a$ and $b$ are **relatively prime** if their greatest common divisor is $1$.

The integers $a_{1}, a_{2}, \cdots, a_{n}$ are **pairwise relatively prime** if $\gcd (a_{i}, a_{j}) = 1$ whenever $1 \le i < j \le n$.

### Definition 5 - Least Common Multiple

The **least common multiple** of the positive integers $a$ and $b$ is the smallest positive integer that is divisible by both $a$ and $b$. It is denoted by

$$
\text{lcm} (a,b)
$$

### Theorem 5

Let $a$ and $b$ be positive integers. Then

$$
ab = \gcd (a,b) \cdot \text{lcm} (a,b)
$$


