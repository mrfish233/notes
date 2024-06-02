# 2 Basic Structures - Sets

## 2.1 Sets

### 2.1.1 Introduction

#### Definition: Set

A set is an unordered collection of distinct objects, called *elements* or members of the set. A set is said to contain its elements.

- $a$ is an element of set $A$: $a \in A$
- $a$ is not an element of set $A$: $a \notin A$

The **roaster method** to describe a set: $A = \{a,b,c,d\}$

An **empty set** (or null set) is denoted by $\emptyset$ or $\{ \ \}$. A set with one element is called _singleton set_.

#### Definition: Equality of Sets

Two sets are equal if and only if they have the same elements. Therefore, if $A$ and $B$ are sets, then $A$ and $B$ are equal if and only if $\forall x (x \in A \leftrightarrow x \in B)$.

If $A$ is equal to $B$, then we write $A = B$.

### 2.1.3 Subsets

#### Definition: Subsets

The set $A$ is a subset of $B$ ($A \subseteq B$), and $B$ is a superset of $A$ ($B \supseteq A$), if and only if every element of $A$ is also an element of $B$. That is,

$$
\forall x (x \in A \to x \in B)
$$

To show that $A \subseteq B$, show that is $x$ belongs to $A$ then $x$ also belongs to $B$. To show that $A \nsubseteq B$, find a single $x \in A$ such that $x \notin B$.

If $A$ is a subset of $B$ but $A \ne B$, then $A$ is a **proper subset** of $B$, denoted by $A \subset B$.

$$
\forall x (x \in A \to x \in B) \land \exists x (x \in B \land x \notin A)
$$

#### Theorem 1

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

#### Showing Equal Sets

To show that two sets $A$ and $B$ are equal, show that $A \subseteq B$ and $B \subseteq A$.

### 2.1.4 The Size of a Set

#### Definition: Finite Set and Infinite Set

Let $S$ be a set. If there are exactly $n$ district elements in $S$ where $n$ is an nonnegative integer, we say that $S$ is a **finite set** and $n$ in the **cardinality** of $S$. The cardinality of $S$ is denoted by $|S|$.

A set is said to be **infinite** if it is not finite.

### 2.1.5 Power Sets

#### Definition: Power Sets

Given a set $S$, the **power set** of $S$ is the set of all subsets of the set $S$. The power set of $S$ is denoted by $\mathcal{P}(S)$.

### 2.1.6 Cartesian Products

#### Definition: Ordered n-tuple

The **ordered n-tuple** $(a_{1}, a_{2}, \cdots, a_{n})$ is the ordered collection that has $a_{1}$ as its first element, ..., and $a_{n}$ as its $n$th element.

#### Definition: Cartesian Product of Two Sets

Let $A$ and $B$ be sets. The **Cartesian product** of $A$ and $B$, denoted by $A \times B$, is the set of all ordered pairs $(a,b)$, which is

$$
A \times B = \set{(a, b) \mid a \in A \land b \in B}
$$

#### Definition: Cartesian Product of n Sets

The **Cartesian product** of the sets $A_{1}, A_{2}, \cdots, A_{n}$, denoted by $A_{1} \times A_{2} \times \cdots \times A_{n}$, is the set of ordered n-tuples $(a_{1}, a_{2}, \cdots, a_{n})$, where $a_{i}$ belongs to $A_{i}, i = 1, 2, \cdots, n$. In other words,

$$
A_{1} \times A_{2} \times \cdots \times A_{n} =
\set{(a_{1}, a_{2}, \cdots, a_{n}) \mid a_{i} \in A_{i}, i = 1, 2, \cdots, n}.
$$

## 2.2 Set Operations

### 2.2.1 Introduction

#### Definition: Union of Set

Let $A$ and $B$ be sets. The **union** of the sets $A$ and $B$, denoted by $A \cup B$, is the sets that contains elements in either $A$ or $B$.

#### Definition: Intersection of Set

Let $A$ and $B$ be sets. The **intersection** of the sets $A$ and $B$, denoted by $A \cap B$, is the sets that contains elements in both $A$ or $B$.

#### Definition: Disjoint of Set

Two sets are called **disjoint** if their intersection is the empty set.

#### Definition: Difference of Set

Let $A$ and $B$ be sets. The **difference** of $A$ and $B$, denoted by $A - B$, is the set containing those elements that are in $A$ but not in $B$. It is also called the **complement of $B$ with respect to $A$**.

#### Definition: Complement of Set

Let $U$ be the universal set. The **complement** of the set $A$, denoted by $\bar{A}$, is $U - A$.

### 2.2.3 Generalized Unions and Intersections

#### Definition: Union of Collection of Sets

The **union** of a collection of sets is the set that contains those elements that are members of at lease one set in the collection.

We use the notation

$$
A_{1} \cup A_{2} \cup \cdots \cup A_{n} = \bigcup_{i=1}^{n} A_{i}
$$

to denote the union of the sets $A_{1}, A_{2}, \cdots, A_{n}$.

#### Definition: Intersection of Collection of Sets

The **intersection** of a collection of sets is the set that contains those elements that are members of all the sets in the collection.

We use the notation

$$
A_{1} \cap A_{2} \cap \cdots \cap A_{n} = \bigcap_{i=1}^{n} A_{i}
$$

to denote the intersection of the sets $A_{1}, A_{2}, \cdots, A_{n}$.

## 2.3 Functions

### 2.3.1 Introduction

#### Definition: Function

Let $A$ and $B$ be nonempty sets. A **function** $f$ from $A$ to $B$ is an assignment of exactly one element of $B$ to each element of $A$. We write $f(a) = b$ if $b$ is the unique element of $B$ assigned by the function $f$ to the element $a$ of $A$.

If $f$ is a function from $A$ to $B$, we write $f: A \to B$.

Functions are sometimes called **mappings** or **transformations**.

#### Definition: Domain, Codomain, Image, Preimage, Range

If $f$ is a function from $A$ to $B$, $A$ is the **domain** of $f$ and $B$ is the **codomain** of $f$. If $f(a) = b$, then $b$ is the **image** of $a$ and $a$ is the **preimage** of $b$.

The **range** or **image** of $f$ is the set of all images of elements of $A$.

#### Definition: Addition and Multiplication of Function

Let $f_{1}$ and $f_{2}$ be functions from $A$ to $\mathbf{R}$. Then $f_{1} + f_{2}$ and $f_{1}f_{2}$ are also functions from $A$ to $\mathbf{R}$ defined for all $x \in A$ by

$$
\begin{align}
(f_{1} + f_{2})(x) &= f_{1}(x) + f_{2}(x), \\
(f_{1}f_{2})(x) &= f_{1}(x) f_{2}(x).
\end{align}
$$

#### Definition: Image of Function

Let $f$ be a function from $A$ to $B$ and let $S$ be a subset of $A$. The **image** of $S$ under the function $f$ is the subset of $B$ that consists of the images of the elements of $S$.

$$
f(S) = \set{t \mid \exists s \in S \ (t = f(s))}.
$$

The shorthand set is $\set{f(s) \mid s \in S}$.

### 2.3.2 One-to-One and Onto Functions

#### Definition: One-to-One

A function $f$ is said to be **one-to-one**, or an **injection**, if and only if $f(a) = f(b)$ implies that $a = b$ for all $a$ and $b$ in the domain of $f$. Such function is called **injective**.

We can express that $f$ is one-to-one as $\forall a \forall b (f(a) = f(b) \implies a = b)$.

#### Definition: Onto

A function $f$ from $A$ to $B$ is called **onto**, or a **surjection**, if and only if for every element $b \in B$ there is an element $a \in A$ with $f(a) = b$. Such function is called **surjective**.

It is also expressed as $\forall y \exists x (f(x) = y)$.

#### Definition: Correspondence

The function $f$ is a **one-to-one correspondence**, or a **bijection**, it it is both one-to-one and onto. Such function is called **bijective**.

#### Summary of Functions

Suppose that $f: A \to B$,

1. To show that $f$ is *injective*, show that if $f(x) = f(y)$ for any $x, y \in A$, then $x = y$.
2. To show that $f$ is *not injective*, find $x, y \in A$ such that $x \ne y$ and $f(x) = f(y)$.
3. To show that $f$ is *surjective*, consider an arbitrary element $y \in B$ and find an element $x \in A$ such that $f(x) = y$.
4. To show that $f$ is *not surjective*, find a particular $y \in B$ such that $f(x) \ne y$ for all $x \in A$.


