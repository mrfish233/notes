## 4.1 Divisibility and Modular Arithmetic

### Definition 1 - Division

If $a$ and $b$ are integers with $a \ne 0$, we say that **$a$ divides $b$** if there is an integer $c$ such that

$$
b = ac.
$$

When $a$ divides $b$, $a$ is a **factor** or **divisor** of $b$, and that $b$ is a multiple of $a$. The notation of $a$ divides $b$ is $a \ | \ b$, and we write $a \ \not \mid b$ when $a$ does not divide $b$.

### Theorem 1

Let $a, b, c$ be integers, where $a \ne 0$. Then

$$
\begin{align}
\text{(i)} & \text{ if } a \ | \ b \text{ and } a \ | \ c, \text{ then } a \ | \ (b+c); \\
\text{(ii)} & \text{ if } a \ | \ b, \text{ then } a \ | \ bc \text{ for all integers } c; \\
\text{(iii)} & \text{ if } a \ | \ b \text{ and } b \ | \ c, \text{ then } a \ | \ c.
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

If $a$ and $b$ are integers and $m$ is a positive integer, then $a$ is *congruent to* $b$ *modulo* $m$ if $m$ divides $a-b$, that is $m \ | \ (a-b)$. Its notation is

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

### Theorem 3 - Infinite Primes

There are infinitely many primes.

**Proof:** (by [[1 The Foundations - Logic and Proofs#Proofs by Contradiction| Contradiction]])

Assume that there are only finitely many primes, $p_{1}, p_{2}, p_{3}, \cdots, p_{n}$. Let

$$
Q = p_{1} p_{2} p_{3} \cdots p_{n} + 1
$$

By the [[#Theorem - The Fundamental Theorem of Arithmetic|fundamental theorem of arithmetic]], $Q$ is prime or else it can be written as the product of two or more primes. However, none of the primes $p_j$ divides $Q$
