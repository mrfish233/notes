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
