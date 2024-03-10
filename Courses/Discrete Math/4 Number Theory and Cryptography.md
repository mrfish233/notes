# 4 Number Theory and Cryptography

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

**Proof:**

$\text{(i)}$ Suppose that $a \mid b$ and $a \mid c$, then there are integers $s$ and $t$ with $b = as$ and $c = at$. Hence,

$$
b + c = as + at = a(s + t)
$$

Therefore $a$ divides $b + c$.

$\text{(iii)}$ Suppose that $a \mid b$ and $b \mid c$, then there are integers $s$ and $t$ with $b = as$ and $c = bt$. Hence,

$$
c = bt = (as)t = a(st).
$$

Therefore $a$ divides $c$.

### Theorem 2 - The Division Algorithm

Let $a$ be an integer and $d$ a positive integer. Then there are unique integers $q, r$ with $0 \le r < d$, such that

$$
a = dq + r.
$$

### Definition 2

In the [Division Algorithm](#Theorem%202%20-%20The%20Division%20Algorithm), $d$ is called the **divisor**, $a$ is called the **dividend**, $q$ is called the **quotient**, and $r$ is called the **remainder**. The notation

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

### Theorem 3 - Equivalence of Congruence

Let $a$ and $b$ be integers, and let $m$ be a positive integer. Then $a \equiv b \pmod{m}$ if and only if

$$
a \bmod m = b \bmod m.
$$

**Proof:**

*(Forward Proof)* Suppose $a \equiv b \pmod{m}$, then by [definition of congruence](#Definition%203%20-%20Congruence), $m \mid (a-b)$, which exists an integer $k$ such that

$$
a - b = km. \tag{1}
$$

Let $a = k_{1}m + r_{1}$ and $b = k_{2}m+ r_{2}$ for some integers $k_{1}, k_{2}, r_{1}, r_{2}$ and $0 \le r_{1}, r_{2} < m$ (by [Division Algorithm](#Theorem%202%20-%20The%20Division%20Algorithm)). Then

$$
\begin{align}
a - b &= (k_{1}m + r_{1}) - (k_{2}m + r_{2}) \\
a - b&= (k_{1} - k_{2})m + (r_{1} - r_{2}). \tag{2}
\end{align}
$$

As $k, k_{1}, k_2$ are arbitrary positive integers, we can assume that $k = k_{1} - k_{2}$. Then by $(1)$ and $(2)$, we have

$$
\begin{align}
a - b &= a - b + (r_{1} - r_{2}) \\
0 &= r_{1} - r_{2} \\
r_{1} &= r_{2}
\end{align}
$$

This shows that $a \bmod m = b \bmod m$.

*(Backward Proof)* Let $a = k_{1}m + r_{1}$ and $b = k_{2}m+ r_{2}$ for some integers $k_{1}, k_{2}, r_{1}, r_{2}$ and $0 \le r_{1}, r_{2} < m$. As $a \bmod m = b \bmod m$, then by [definition of remainder](#Definition%202), $r_{1} = r_{2}$. Then

$$
\begin{align}
a - b &= (k_{1}m + r_{1}) - (k_{2}m + r_{2}) \\
&= (k_{1} - k_{2})m + (r_{1} - r_{2}) \\
&= (k_{1} - k_{2})m + 0 \\
&= (k_{1} - k_{2})m
\end{align}
$$

This shows that $m \mid (a-b)$ by [definition of division](#Definition%201%20-%20Division). Therefore, by [definition of congruence](#Definition%203%20-%20Congruence),

$$
a \equiv b \pmod{m}.
$$

This completes our proof.

### Theorem 4

Let $a$ and $b$ be integers, and let $m$ be a positive integer. Then $a \equiv b \pmod{m}$ if and only if there exists an integer $k$ such that

$$
a = b + km.
$$

### Theorem 5 - Addition and Multiplication Rules

Let $m$ be a positive integer. If $a \equiv b \pmod{m}$ and $c \equiv d \pmod{m}$, then

$$
\begin{alignat}1
a + c &\equiv b + d &&\pmod{m}; \\
ac &\equiv bd &&\pmod{m}
\end{alignat}
$$

**Proof:**

*(by [direct proof](1%20The%20Foundations%20-%20Logic%20and%20Proofs.md#Direct%20Proofs))* Since $a \equiv b \pmod{m}$ and $c \equiv d \pmod{m}$, by [Theorem 4](#Theorem%204) there exist integers $k_{1}$ and $k_{2}$ with $b = a + k_{1}m$ and $d = c + k_{2}m$. Hence,

$$
\begin{align}
b + d &= (a + k_{1}m) + (c + k_{2}m), \text{ and} \\
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
\begin{alignat}1
a + c &\equiv b + d &&\pmod{m}, \text{ and} \\
ac &\equiv bd &&\pmod{m}
\end{alignat}
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

### Definition 4 - Prime and Composite

An integer $p$ greater than $1$ is called **prime** is the only positive factors of $p$ are $1$ and $p$. A positive integer that is greater that $1$ and is not prime is called **composite**.

### Theorem 6 - The Fundamental Theorem of Arithmetic

Every integer greater than $1$ can be written uniquely as a prime or as the product of two or more primes, where the prime factors are written in order of nondecreasing size.

**Example:**

1. $100 = 2 \cdot 2 \cdot 5 \cdot 5 = 2^{2}5^{2}$
2. $641 = 641$

### Theorem 7 - Composite Integer

If $n$ is a [composite integer](#Definition%204%20-%20Prime%20and%20Composite), then $n$ has a prime divisor less than or equal to $\sqrt{n}$.

#### The Sieve of Eratosthenes

This is used to find all primes not exceeding a specified positive integer. It does so by iteratively marking as **composite** the multiples of each prime, starting with the first prime number, 2. Once all the multiples of each discovered prime have been marked as composites, the remaining unmarked numbers are primes. (from [Wikipedia](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes))

### Theorem 8 - Euclid's Theorem

There are infinitely many primes.

**Proof:**

*(by [contradiction](1%20The%20Foundations%20-%20Logic%20and%20Proofs.md#Proofs%20by%20Contradiction))* Assume $p_{1}, p_{2}, p_{3}, \cdots, p_{n}$ is a finite list of prime numbers. Let

$$
P = p_{1} p_{2} p_{3} \cdots p_{n} \quad \text{ and } \quad
Q = P + 1
$$

By [Theorem 6 - The Fundamental Theorem of Arithmetic](#Theorem%206%20-%20The%20Fundamental%20Theorem%20of%20Arithmetic), $Q$ is prime or else it can be written as the product of two or more primes.

- If $Q$ is prime, then there is at lease one or more prime that is not in the list $p_{1}, p_{2}, p_{3}, \cdots, p_{n}$, namely, $Q$ itself.
- If $Q$ is not prime, then there exists $p_{j}$ is a prime factor of $Q$. $p_j$ can't be any of $p_{1}, p_{2}, p_{3}, \cdots, p_{n}$ since $Q$ has remainder of $1$ when divided by each $p_i$. Therefore $p$ is a prime not on our list.

Hence, there is a prime not in the list $p_{1}, p_{2}, p_{3}, \cdots, p_{n}$ in both cases above. This is a **contradiction** because we assume that we have listed all the primes. Consequently, there are infinitely many primes.

### Theorem 9 - The Prime Number Theorem

The ratio of $\pi{(x)}$ (the number of primes not exceeding $x$) and $\displaystyle\frac{x}{\ln x}$ approaches $1$ as $x$ grows without bound.

### Definition 5 - Greatest Common Divisor

Let $a$ and $b$ be integers, not both zero. The largest integer $d$ such that $d \mid a$ and $d \mid b$ is called the **greatest common divisor** of $a$ and $b$. The notation is

$$
d = \gcd (a,b)
$$

### Definition 6 - Relatively Prime

The integers $a$ and $b$ are **relatively prime** if their greatest common divisor is $1$.

The integers $a_{1}, a_{2}, \cdots, a_{n}$ are **pairwise relatively prime** if $\gcd (a_{i}, a_{j}) = 1$ whenever $1 \le i < j \le n$.

### Definition 7 - Least Common Multiple

The **least common multiple** of the positive integers $a$ and $b$ is the smallest positive integer that is divisible by both $a$ and $b$. It is denoted by

$$
\text{lcm} (a,b)
$$

### Theorem 10 - GCD and LCM

Let $a$ and $b$ be positive integers. Then

$$
ab = \gcd (a,b) \cdot \text{lcm} (a,b)
$$

### The Euclidean Algorithm

This algorithm is an efficient method of finding the greatest common divisor.

**Example:** $\gcd (91, 287)$

$$
\begin{align}
287 &= 91 \cdot 3 + 14 \\
91 &= 14 \cdot 6 + 7 \\
14 &= 7 \cdot 2 + 0
\end{align}
$$

Therefore $\gcd (91, 287) = 7$.

#### Lemma 1

Let $a = bq + r$, where $a, b, q, r$ are integers. Then

$$
\gcd (a,b) = \gcd (b,r)
$$

**Proof:**

If we can show that **all** the common divisors of $a$ and $b$ are the same as the common divisors of $b$ and $r$, we will have shown that $\gcd (a,b) = \gcd (b,r)$. That is, we show that both $\gcd (a, b) \le \gcd (b, r)$ and $\gcd (b, r) \le \gcd (a, b)$ hold.

Suppose integer $d_{1}$ is a common divisor of $a$ and $b$. Let $a = k_{1}d_{1}$ and $b = k_{2}d_{1}$, where $k_{1}, k_{2} \in \mathbb{Z}$. Then

$$
\begin{align}
r &= a - bq \\
&= k_{1}d_{1} - k_{2}d_{1}q \\
&= d_{1}(k_{1} - k_{2}q)
\end{align}
$$

This implies that every common divisor of $a$ and $b$ is a divisor of $r$. Therefore $\gcd (a, b) \le \gcd (b, r)$.

Similarly, suppose $d_{2}$ is a common divisor of $b$ and $r$. Let $b = k_{3}d_{2}$ and $r = k_{4}d_{2}$, where $k_{3}, k_{4} \in \mathbb{Z}$. Then

$$
\begin{align}
a &= bq + r \\
&= k_{3}d_{2}q + k_{4}d_{2} \\
&= d_{2} (k_{3}q + k_{4})
\end{align}
$$

This implies that every common divisor of $b$ and $r$ is a divisor of $a$. Therefore $\gcd (b, r) \le \gcd (a, b)$.

Consequently,

$$
\gcd (a,b) = \gcd (b,r).
$$

### Theorem 11 - Bézout's Identity

If $a$ and $b$ are positive integers, then there exist integers $x$ and $y$ such that

$$
\gcd (a,b) = ax + by.
$$

**Proof:**

(Well-ordering Principle: every nonempty set of nonnegative integers has a smallest element. This property is used in this proof.)

Let $S$ be a set of positive integers of the form $ax + by$, where $x, y$ are integers:

$$
S = \{ax + by \mid x,y \in \mathbb{Z}, ax + by > 0 \}
$$

The set is **nonempty** since it contains either $a$ or $b$ with $x = 1, y = 0$ and $x = 0, y = 1$. Since $S$ is nonempty set of positive integers, by **well-ordering principle**, there exists a smallest element $d_0$ such that

$$
d_{0} = ax_{0} + by_{0}, \quad x_{0}, y_{0} \in \mathbb{Z}.
$$

We can now prove the theorem by proving $\gcd (a,b) = d_{0}$. To prove $d_{0}$ is greatest common divisor of $a$ and $b$, we must prove that

1. $d_0$ is common divisor of $a$ and $b$, or $d_{0} \mid a$ and $d_{0} \mid b$.
2. For any other common divisor $c$, one has $c \le d_{0}$, or

$$
\forall c \ (c \mid a) \land (c \mid b) \implies c \mid d_{0}
$$

*(Proof  1.)* First, let $a = kd_{0} + r, k \in \mathbb{Z}, 0 \le r < d_{0}$ (by [The Division Algorithm](#Theorem%202%20-%20The%20Division%20Algorithm)). Then

$$
\begin{align}
r &= a - kd_{0} \\
&= a - k(ax_{0} + by_{0}) \\
&= a(1 - kx_{0}) + b(ky_{0}).
\end{align}
$$

If $r \ne 0$, then $r \in S$ since $r$ is in the form of $ax + by$. This *contradicts* with our assumption of $d_{0}$ is the smallest element in $S$. Therefore $r = 0$ and

$$
a = kd_{0}+ r = kd_0
$$

which shows that $d_{0} \mid a$ (by definition of [division](#Definition%201%20-%20Division)). Similarly $d_{0}$ is also a divisor of $b$ and therefore $d_{0} \mid a$ and $d_{0} \mid b$.

*(Proof  2.)* Next, let $c$ be a common divisor of $a$ and $b$, that is, there exist $k_{1}$ and $k_{2}$ such that $a = ck_{1}$ and $b = ck_{2}$. Then

$$
\begin{align}
d_{0} &= ax_{0} + by_{0} \\
&= (ck_{1})x_{0} + (ck_{2})y_{0} \\
&= c(k_{1}x_{0} + x_{2}y_{0}).
\end{align}
$$

This shows that $c \mid d_{0}$ and therefore complete our proofs.

#### Lemma 2

If $a, b, c$ are positive integers such that $\gcd (a,b) = 1$ and $a \mid bc$, then $a \mid c$.

**Proof:**

As $\gcd (a,b) = 1$, by [Bézout's Identity](#Theorem%2011%20-%20Bézout's%20Identity) there are integers $x, y$ such that $ax + by = 1$. Multiplying both sides by $c$ and we have

$$
axc + byc = c.
$$

As $a \mid bc$, by [Definition 1](#Definition%201%20-%20Division) there is an integer $k$ such that $bc = ak$. Substitute this statement into statement above and we have

$$
\begin{align}
axc + byc &= c \\
axc + y(ak) &= c \\
a(xc + yk) &= c
\end{align}
$$

This implies that $a$ is divisible by $c$, which is $c \mid a$. This complete our proof.

#### Lemma 3

If $p$ is a prime and $p \mid a_{1}a_{2}\cdots a_{n}$, where each $a_{i}$ is an integer, then $p \mid a_{i}$ for some $i$.

- [ ] proof DM Lemma 3

### Theorem 12 - Relation of Congruence and GCD

Let $m$ be a positive integer and let $a, b, c$ be integers. If $ac \equiv bc \pmod{m}$ and $\gcd(c, m) = 1$, then $a \equiv b \pmod{m}$.

**Proof:**

As $ac \equiv bc \pmod{m}$, then $m \mid ac - bc = c(a-b)$. By [Lemma 2](#Lemma%202), because $\gcd (c, m) = 1$, then

$$
m \mid a-b.
$$

Therefore $a \equiv b \pmod{m}$.

## 4.4 Solving Congruences

### Linear Congruences

A congruence of the form

$$
ax \equiv b \pmod{m}
$$

where $m \in \mathbb{Z^{+}}, a,b \in \mathbb{Z}$ and $x$ is a variable, is called a **linear congruence**.

To solve $x$, one method is to find an integer $\bar{a}$ such that $a\bar{a} \equiv b \pmod{m}$ if it exists. The integer $\bar{a}$ is said to be an **inverse** of $a$ modulo $m$.

### Theorem 13 - Inverse for Linear Congruences

If $a$ and $m$ are relatively prime integers and $m > 1$, then $\bar{a}$, an inverse of $a$ modulo $m$ exists. That is,

$$
a \bar{a} \equiv 1 \pmod{m}
$$

Furthermore, $\bar{a}$ is **unique** modulo $m$.

($\bar{a}$ unique modulo $m$ means there exists unique $\bar{a} < m$ is an inverse of $a$ modulo $m$ and every other inverse of $a$ modulo $m$, $\bar{b}$ is congruent to $\bar{a}$ modulo $m$, that is $\bar{b} \equiv \bar{a} \pmod{m}$.)

**Proof:**

*(Proof of Existence)* As $\gcd (a, m) = 1$, by [Theorem 11 - Bézout's Identity](#Theorem%2011%20-%20Bézout's%20Identity), there are integers $x, y$ such that

$$
ax + my = 1.
$$

By [Theorem 3](#Theorem%203%20-%20Equivalence%20of%20Congruence), this implies that

$$
\begin{align}
(ax + my) \bmod m &= 1 \bmod m \\
ax + my &\equiv 1 \pmod{m}.
\end{align}
$$

Because $my \equiv 0 \pmod{m}$, by [Theorem 5](#Theorem%205%20-%20Addition%20and%20Multiplication%20Rules), it follows that

$$
ax \equiv 1 \pmod{m}.
$$

This shows that there exists an integer $x$  such that it is the inverse of $a$ modulo $m$.

*(Proof of Uniqueness)* Assume that there are 2 solutions $x_{1}, x_{2} \ (0 \le x_{1}, x_{2} < m)$ of the congruence $ax \equiv 1 \pmod{m}$. Then

$$
ax_{1} \equiv 1 \pmod{m} \qquad \text{and} \qquad
ax_{2} \equiv 1 \pmod{m}
$$

This shows that $ax_{1} \equiv ax_{2} \equiv 1 \pmod{m}$. By [Theorem 12](#Theorem%2012%20-%20Relation%20of%20Congruence%20and%20GCD), as $\gcd (a, m) = 1$, then

$$
x_{1} \equiv x_{2} \pmod{m}.
$$

Therefore $x_{1} = x_{2}$. This proof the inverse of modulo $m$ is unique.

### Theorem 14 - Chinese Remainder Theorem

Let $m_{1}, m_{2}, \cdots, m_{n}$ be *pairwise relatively prime* positive integers greater than $1$ and $a_{1}, a_{2}, \cdots, a_{n}$ arbitrary integers. Then the system

$$
\begin{align}
x &\equiv a_{1} \pmod{m_{1}}, \\
x &\equiv a_{1} \pmod{m_{1}}, \\
& \ \vdots \\
x &\equiv a_{n} \pmod{m_{n}}
\end{align}
$$

has a unique solution modulo $m = m_{1}m_{2} \cdots m_{n}$.

**Proof:**

*(Proof of Existence)* let $M_{k} = \displaystyle\frac{m}{m_{k}}$ for $k = 1, 2, \cdots, n$. As $\gcd (m_{i}, m_{j}) = 1$ whenever $i \ne j$, then

$$
\gcd (m_{k}, M_{k}) = 1.
$$

By [Theorem 13](#Theorem%2013%20-%20Inverse%20for%20Linear%20Congruences), there exists an integer $y_{k}$ such that

$$
M_{k} y_{k} \equiv 1 \pmod{m_{k}}.
$$

Then, construct a simultaneous solution

$$
\begin{align}
x &= \sum\limits_{k=1}^{n} a_{k}M_{k}y_{k} \\
&= a_{1}M_{1}y_{1} + a_{2}M_{2}y_{2} + \cdots + a_{n}M_{n}y_{n}.
\end{align}
$$

Because $M_{j} \equiv 0 \pmod{m_k}$ whenever $j \ne k$ and $M_{k} y_{k} \equiv 1 \pmod{m_{k}}$, by [Theorem 5](#Theorem%205%20-%20Addition%20and%20Multiplication%20Rules),

$$
x \equiv a_{k}M_{k}y_{k} \equiv a_{k} \pmod{m_{k}}, \quad k = 1, 2, \cdots, n.
$$

This shows that $x$ is a simultaneous solution to the $n$ congruences.

*(Proof of Uniqueness)* Suppose there are 2 solutions $x_{1}$ and $x_{2}$ to the $n$ congruences, that is

$$
x_{1} \equiv a_{k} \pmod{m_{k}} \qquad \text{and} \qquad
x_{2} \equiv a_{k} \pmod{m_{k}}, \quad k \in \{1, 2, \cdots, n\}.
$$

Then by [Theorem 5](#Theorem%205%20-%20Addition%20and%20Multiplication%20Rules),

$$
x_{1} - x_{2} \equiv 0 \pmod{m_{k}}.
$$

This shows that $m_{k} \mid (x_{1} - x_{2})$ for $k = 1, 2, \cdots, n$. Since $\gcd (m_{i}, m_{j}) = 1$ whenever $i \ne j$, then it follows that $m_{1}m_{2} \cdots m_{n} \mid (x_{1} - x_{2})$, or

$$
x_{1} \equiv x_{2} \pmod{m_{1}m_{2} \cdots m_{n}}.
$$

Therefore the solution is unique modulo $m_{1}m_{2} \cdots m_{n}$.

### Theorem 15 - Fermat's Little Theorem

If $p$ is prime and $a$ is an integer not divisible by $p$, then

$$
a^{p-1} \equiv 1 \pmod{p}.
$$

Furthermore, for every integer $a$ we have

$$
a^{p} \equiv a \pmod{p}.
$$

(Some amazing proofs can be found at this [link](https://artofproblemsolving.com/wiki/index.php/Fermat%27s_Little_Theorem).)

**Proof:**

Proving steps:

1. First by proving if integers $i, j \in \{1, 2, 3, \cdots, p-1\}, i \ne j$, then $ai \not \equiv aj \pmod{p}$.
2. If integer $k \in \{1, 2, 3, \cdots, p-1\}$, then $ak \not \equiv 0 \pmod{p}$. Use this statement and statement above to prove that

$$
(p-1)! \equiv a^{p-1} (p-1)! \pmod{p}.
$$

3. Use the statement above to prove that $a^{p-1} \equiv 1 \pmod{p}$.

*(Proof 1.)* Suppose $a$ is not divisible by $p$. Let the integers $i$ and $j$ where $i, j \in \{1, 2, 3, \cdots, p-1\}$. If $i \ne j$, then $ai \not \equiv aj \pmod{p}$.

If not, assume that when $i \ne j$, we have $ai \equiv aj \pmod{p}$. By [Definition 3](#Definition%203%20-%20Congruence), we have

$$
p \mid a(i-j)
$$

As $\gcd (a, p) = 1$, by [Lemma 2](#Lemma%202), we have $p \mid (i - j)$. Because of $i < p, j < p, |i-j| < p$, for $p \mid (i - j)$ to be valid, we must have

$$
i - j = 0 \quad \text{or} \quad i=j.
$$

This contradicts with our assumption of $i \ne j$. Therefore $ai \not \equiv aj \pmod{p}$.

*(Proof 2.)* Let $k \in \{1, 2, \cdots, p-1\}$. As $p$ is a prime number, and $\gcd (a, p) = 1$, it shows that

$$
a \cdot k\equiv x_{k} \pmod{p}, \quad x_{k}\in \{1, 2, \cdots, p-1\}.
$$

By the statement $ai \not \equiv aj \pmod{p}$ when $i \ne j$, we know that $x_{k_{1}} \ne x_{k_{2}}$ when $k_{1} \ne k_{2}$. Hence, if we multiply $a, 2a, 3a, \cdots, (p-1)a$, we must have

$$
\begin{align}
a \cdot 2a \cdot 3a \cdot \ldots \cdot (p-1)a &\equiv x_{1}x_{2}x_{3} \cdots x_{p-1} \\
&\equiv 1 \cdot 2 \cdot 3 \cdot \ldots \cdot (p-1) \pmod{p}.
\end{align}
$$

Therefore we have

$$
a^{p-1} (p-1)! \equiv (p-1)! \pmod{p}. \tag{2}
$$

*(Proof 3.)* Let $a \in \{1, 2, 3, \cdots, p-1\}$. Then $p$ is not divisible by any $a$, that is

$$
p \not \mid a, \quad a \in \{1, 2, 3, \cdots, p-1\}.
$$

By contraposition of [Lemma 3](#Lemma%203), we have

$$
p \not \mid 1 \cdot 2 \cdot 3 \cdot \ldots \cdot (p-1).
$$

This implies that $\gcd (p, (p-1)!) = 1$. Combine the result from $(2)$ and [Theorem 12](#Theorem%2012%20-%20Relation%20of%20Congruence%20and%20GCD), we have

$$
a^{p-1} \equiv 1 \pmod{p}.
$$

This complete our proof.
