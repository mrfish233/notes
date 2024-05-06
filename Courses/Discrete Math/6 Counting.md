# Counting

## 6.1 The Basics of Counting

### The Product Rule

Suppose that a procedure can be broken down into a sequence of two tasks. If there are $n_{1}$ ways to do the first task and for each of $n_{1}$ ways, there are $n_{2}$ ways to do the second task, then there are

$$
n_{1}n_{2}
$$

ways to do the procedure.

### The Sum Rule

If a task can be done either in one of $n_{1}$ ways or in one of $n_{2}$ ways, and none of the set of $n_{1}$ ways is the same as any of set of $n_{2}$ ways, then there are

$$
n_{1} + n_{2}
$$

ways to do the task.

### The Subtraction Rule

If a task can be done in either $n_{1}$ ways or $n_{2}$ ways, then the number of ways to do the task is

$$
n_{1} + n_{2} - n_{12}
$$

where $n_{12}$ is the number of ways to do the task that are common to the two different ways.

This is also known as the **principle of inclusion-exclusion**.

**Example:** there are $|A_{1}|$ ways to select element from $A_{1}$ and $|A_{2}|$ ways to select element from $A_{2}$, then

$$
|A_{1} \cup A_{2}| = |A_{1}| + |A_{2}| - |A_{1} \cap A_{2}|
$$

### The Division Rule

There are $n/d$ ways to do a task if it can be done using a procedure that can be carried out in $n$ ways, and for every way $w$, exactly $d$ of the $n$ ways correspond to way $w$.

**Example:** Total ways to seat 4 people around a circular table.

There are total of $4! = 24$ ways to order the given 4 people for these seats, without considering the same seating's around the circular table. Since the following seats are considered as same:

$$
1234, 2341, 3412, 4123
$$

By division rule there are $24 / 4 = 6$ different seating arrangements of 4 people around the circular table.

## 6.2 The Pigeonhole Principle

### Theorem 1 - The Pigeonhole Principle

If $k$ is a positive integer and $k + 1$ or more objects are placed into $k$ boxes, then there is at least one box containing two or more of the objects.

The principle is also called the **Dirichlet drawer principle**.

#### Corollary of Theorem 1

A function $f$ from a set with $k +1$ or more elements to set with $k$ elements is not one-to-one.

### Theorem 2 - The Generalized Pigeonhole Principle

If $N$ objects are placed into $k$ boxes, then there is at least one box containing at least $\lceil N/k \rceil$ objects.

### Theorem 3 - Strictly Increasing or Decreasing

Every sequence of $n^{2} + 1$ distinct real numbers contains a subsequence of length $n + 1$ that is either strictly increasing or strictly decreasing.

## 6.3 Permutations and Combinations

### Theorem 4 - Permutation

If $n$ is a positive integer and $r$ is an integer with $1 \le r \le n$, then there are

$$
P(n,r) = n(n-1)(n-2) \cdots (n-r+1)
$$

$r$-permutations of a set with $n$ distinct elements.

#### Corollary 2

If $n$ and $r$ are integers with $0 \le r \le n$, then

$$
P(n,r) = \frac{n!}{(n-r)!}.
$$

### Theorem 5 - Combination

The number of $r$-combinations of a set with $n$ elements, where $n$ is a nonnegative integer and $r$ is an integer with $0 \le r \le n$, equals

$$
C(n,r) = \frac{n!}{r! \ (n-r)!}
$$

#### Corollary 3

Let $n$ and $r$ be integers with $0 \le r \le n$, then

$$
C(n,r) = C(n,n-r).
$$

### Definition 1 - Combinatorial Proof

A **combinatorial proof** of an identity is a proof that uses counting arguments to prove that both sides of the identity count the same objects but in different ways, called *double counting proof*.
Another way of combinatorial proof is showing that there is a bijection between the sets of objects counted by the two sides of the identity, called *bijective proof*.

## 6.4 Binomial Coefficients and Identities

### Theorem 6 - The Binomial Theorem

Let $x, y$ be variables, and let $n$ be a nonnegative integer, then

$$
\begin{align}
(x + y)^{n} &= \sum\limits_{r=0}^{n} \binom{n}{r} x^{n-r}y^{r} \\
&= \binom{n}{0} x^{n} + \binom{n}{1} x^{n-1}y + \cdots + \binom{n}{n-1}xy^{n-1} + \binom{n}{n} y^{n}.
\end{align}
$$

#### Corollary 1 of Theorem 6

Let $n$ be a nonnegative integer. Then

$$
\sum\limits_{k=0}^{n} \binom{n}{k} = 2^{n}.
$$

#### Corollary 2 of Theorem 6

Let $n$ be a positive integer. Then

$$
\sum\limits_{k=0}^{n} (-1)^{k} \binom{n}{k} = 0.
$$

#### Corollary 3 of Theorem 6

Let $n$ be a nonnegative integer. Then

$$
\sum\limits_{k=0}^{n} 2^{k} \binom{n}{k} = 3^{n}.
$$

### Theorem 7 - Pascal's Identity

Let $n, k$ be positive integers with $n \ge k$. Then

$$
\binom{n+1}{k} = \binom{n}{k-1} + \binom{n}{k}.
$$

### Theorem 8 - Vandermonde's Identity

Let $m, n, r$ be nonnegative integers with $r$ not exceeding either $m$ or $n$. Then

$$
\binom{m+n}{r} = \sum\limits_{k=0}^{r} \binom{m}{r-k} \binom{n}{k}.
$$

#### Corollary of Theorem 8

If $n$ is a nonnegative integer, then

$$
\binom{2n}{n} = \sum\limits_{k=0}^{n} \binom{n}{k}^{2}.
$$

### Theorem 9

Let $n$ and $r$ be nonnegative integers with $r \le n$. Then

$$
\binom{n+1}{r+1} = \sum\limits_{k=r}^{n} \binom{k}{r}.
$$

### Theorem 10 - Permutation with Repetition

The number of $r$-permutations of a set of $n$ objects with repetition allowed is $n^r$.

**Proof:** there are $n$ ways to select an element of the set for each of the $r$ positions, hence by product rule there are $n^r$ $r$-permutations when repetition is allowed.

**Example:** A string with length $r$ that contains only 26 uppercase English letters have $26^{r}$ different strings.

### Theorem 11 - Combination with Repetition

The number of $r$-combinations of a set of $n$ objects with repetition allowed is

$$
C(n+r-1, r) = C(n+r-1, n-1).
$$

**Example:** how many solutions does the equation

$$
x_{1} + x_{2} + x_{3} = 11
$$

have, where $x_{1}, x_{2}, x_{3}$ are nonnegative integers?

**Solution:** the solution corresponds to a way of selecting 11 items from a set with 3 elements. Hence the number of solutions is equal to the number of $11$-combinations with repetition allowed from a set with 3 elements, which is

$$
C(3 + 11 - 1, 11) = C(13, 11) = 78.
$$

Assume that $x_{1} \ge 1, x_{2} \ge 2, x_{3} \ge 3$, then there is at least one $x_{1}$, two $x_{2}$, and three $x_{3}$. So the solution is

$$
C(3 + 5 - 1, 5) = C(7, 5) = 21.
$$


