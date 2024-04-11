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

is always true by definition of [implications](1%20The%20Foundations%20-%20Logic%20and%20Proofs.md#Definition%205%20-%20Implication).

$\text{(ii)}$ To show that $S \subseteq S$, we must show that $\forall x (x \in S \to x \in S)$ is true. Then

| $x \in S$ | $x \in S \to x \in S$ |
| --------- | --------------------- |
| T         | T                     |
| F         | T                     |

Therefore $S \subseteq S$ is **true**.

### Definition 4 - Finite Set and Infinite Set
Let $S$ be a set. If there are exactly $n$ district elements in $S$ where $n$ is an nonnegative integer, we say that $S$ is a **finite set** and $n$ in the **cardinality** of $S$. The cardinality of $S$ is denoted by $|S|$.

A set is said to be **infinite** if it is not finite.

### Definition 5 - Power Sets

Given a set $S$, the **power set** of $S$ is the set of all subsets of the set $S$. The power set of $S$ is denoted by $\mathcal{P}(S)$.

### Definition 6 - Ordered n-tuple

The **ordered n-tuple** $(a_{1}, a_{2}, \cdots, a_{n})$ is the ordered collection that has $a_{1}$ as its first element, $a_{2}$ as its second element, $\cdots$, and $a_{n}$ as its $nth$ element.

### Definition 7 - Cartesian Products

Let $A$ and $B$ be sets. The **Cartesian product** of $A$ and $B$, denoted by $A \times B$, is

$$
A \times B = \set{(a, b) \mid a \in A \land b \in B}
$$

## 2.2 Set Operations

### Definition 8 - Union of Set

Let $A$ and $B$ be sets. The **union** of the sets $A$ and $B$, denoted by $A \cup B$, is the sets that contains elements in either $A$ or $B$.

### Definition 9 - Intersection of Set

Let $A$ and $B$ be sets. The **intersection** of the sets $A$ and $B$, denoted by $A \cap B$, is the sets that contains elements in both $A$ or $B$.

### Definition 10 - Disjoint of Set

Two sets are called **disjoint** if their intersection is the empty set.

### Definition 11 - Difference of Set

Let $A$ and $B$ be sets. The **difference** of $A$ and $B$, denoted by $A - B$, is the set containing those elements that are in $A$ but not in $B$. It is also called the **complement of $B$ with respect to $A$**.

### Definition 12 - Complement of Set

Let $U$ be the universal set. The **complement** of the set $A$, denoted by $\bar{A}$, is $U - A$.

### Definition 13 - Union of Collection of Sets

The **union** of a collection of sets is the set that contains those elements that are members of at lease one set in the collection.

We use the notation

$$
A_{1} \cup A_{2} \cup \cdots \cup A_{n} = \bigcup_{i=1}^{n} A_{i}
$$

to denote the union of the sets $A_{1}, A_{2}, \cdots, A_{n}$.

### Definition 14 - Intersection of Collection of Sets

The **intersection** of a collection of sets is the set that contains those elements that are members of all the sets in the collection.

We use the notation

$$
A_{1} \cap A_{2} \cap \cdots \cap A_{n} = \bigcap_{i=1}^{n} A_{i}
$$

to denote the intersection of the sets $A_{1}, A_{2}, \cdots, A_{n}$.
