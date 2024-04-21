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

#### Corollary 1

A function $f$ from a set with $k +1$ or more elements to set with $k$ elements is not one-to-one.

### Theorem 2 - The Generalized Pigeonhole Principle

If $N$ objects are placed into $k$ boxes, then there is at least one box containing at least $\lceil N/k \rceil$ objects.

### Theorem 3

Every sequence of $n^{2} + 1$ distinct real numbers contains a subsequence of length $n + 1$ that is either strictly increasing or strictly decreasing.

### Ramsey Theory



## 6.3
