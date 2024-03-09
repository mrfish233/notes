# 2 Basic Structures - Sets

## 2.1 Sets

### Definition 1 - Set

A set is an unordered collection of distinct objects, called *elements* or members of the set. A set is said to contain its elements.

- $a$ is an element of set $A$: $a \in A$
- $a$ is not an element of set $A$: $a \notin A$

The **roaster method** to describe a set: $A = \{a,b,c,d\}$

An **empty set** (or null set) is denoted by $\emptyset$ or $\{ \ \}$. A set with one element is called _singleton set_.

### Definition 2 - Equality of Sets

Two sets are equal if and only if they have the same elements. Therefore, if $A$ and $B$ are sets, then $A$ and $B$ are equal if and only if $\forall x (x \in A \leftrightarrow x \in B)$.

If $A$ is equal to $B$, then we write $A = B$.

### Definition 3 - Subsets

The set $A$ is a subset of $B$ ($A \subseteq B$), and $B$ is a superset of $A$ ($B \supseteq A$), if and only if every element of $A$ is also an element of $B$. That is,

$$
\forall x (x \in A \to x \in B)
$$

To show that $A \subseteq B$, show that is $x$ belongs to $A$ then $x$ also belongs to $B$. To show that $A \nsubseteq B$, find a single $x \in A$ such that $x \notin B$.

If $A$ is a subset of $B$ but $A \ne B$, then $A$ is a **proper subset** of $B$, denoted by $A \subset B$.

$$
\forall x (x \in A \to x \in B) \land \exists x (x \in B \land x \notin A)
$$

### Theorem 1

For every set $S$, $\text{(i)} \ \emptyset \subseteq S$ and $\text{(ii)} \ S \subseteq S$.

**Proof:**

$\text{(i)}$ To show that $\emptyset \subseteq S$, we must show that $\forall x (x \in \emptyset \to x \in S)$ is true. As empty set contains no elements, $x \in \emptyset$ is always **false**. Therefore

$$
x \in \emptyset \to x \in S
$$

is always true by definition of [](1%20The%20Foundations%20-%20Logic%20and%20Proofs.md#Definition%205%20-%20Implication|implications).

$\text{(ii)}$ To show that $S \subseteq S$, we must show that $\forall x (x \in S \to x \in S)$ is true. Then

| $x \in S$ | $x \in S \to x \in S$ |
| --------- | --------------------- |
| T         | T                     |
| F         | T                      |

Therefore $S \subseteq S$ is **true**.


