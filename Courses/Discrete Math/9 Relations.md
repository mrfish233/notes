# 9 Relations

## 9.1 Relations and Their Properties

### Definition - Binary Relation

Let $A$ and $B$ be sets. A **binary relation** from $A$ to $B$ is a subset of $A \times B$. The notation $aRb$ is used to denote $(a,b) \in R$ and $a \not R b$ is $(a,b) \not \in R$.

### Definition - Relation on a Set

A **relation on a set** $A$ is a relation from $A$ to $A$, or a subset of $A \times A$.

### Properties of Relations

- **Reflexive**: for $a \in A, (a,a) \in R$.
- **Symmetric**: for $a, b \in A, (a,b) \in R \implies (b,a) \in R$.
- **Antisymmetric**: for $a, b \in A, (a,b) \in R \implies (b,a) \notin R$.
- **Transitive**: for $a,b,c \in A, (a,b) \in R \land (b,c) \in R \implies (a,c) \in R$.

### Definition - Composite

Let $R$ be a relation from a set $A$ to a set $B$ and $S$ a relation from $B$ to a set $C$. The **composite** of $R$ and $S$, denoted by $S \circ R$, is the relation consisting of ordered pairs $(a,c)$, where $a \in A, c \in C$, and for which there exists an element $b \in B$ such that $(a,b) \in R$ and $(b,c) \in S$.

### Definition - Self-Relation

Let $R$ be a relation on the set $A$. The powers $R^{n}, n = 1, 2, 3, \cdots$, are defined as

$$
R^{1} = R \quad \text{and} \quad R^{n+1} = R^{n} \circ R.
$$

### Theorem 1 - Transitive Relation

The relation $R$ on a set $A$ is **transitive** if and only if $R^{n} \subseteq R$ for $n = 1, 2, 3, \cdots$.

## 9.5 Equivalence Relations

### 9.5.2 Equivalence Relations

#### Definition - Equivalence Relation

A relation on a set $A$ is called an equivalence relation if it is **reflexive, symmetric, and transitive**.

**Example:** Congruence Modulo $m$

Let the relation $R$ be

$$
R = \set{(a,b) \mid a \equiv b \pmod{m}}
$$

Since $a \equiv a \pmod{m}$, then congruence modulo $m$ is *reflexive*. Suppose $a \equiv b \pmod{m}$, then

$$
\begin{align}
a - b &= km \\
b - a &= (-k)m
\end{align}
$$

By definition we have $b \equiv a \pmod{m}$, therefore congruence modulo $m$ is *symmetric*. Suppose $a \equiv b \pmod{m}$ and $b \equiv c \pmod{m}$, then there exists integers $k, l$ such that $a - b = km$ and $b - c = lm$. Then

$$
\begin{align}
(a-b) + (b-c) &= km - lm \\
a-c &= (k-l)m
\end{align}
$$

By definition we have $a \equiv c \pmod{m}$, therefore congruence modulo $m$ is **transitive**. Therefore congruence modulo $m$ is an equivalence relation.

#### Definition - Equivalent

Two elements $a$ and $b$ that are related by an equivalence relation are called **equivalent**. The notation $a \sim b$  is used to denote $a$ and $b$ are equivalent elements with respect to a particular equivalence relation.

### 9.5.3 Equivalence Classes

#### Definition: Equivalence Classes

Let $R$ be an equivalence relation on a set $A$. The set of all elements that are related to an element $a$ of $A$ is called the **equivalence class** of $a$, denoted by $[a]_{R}$. The notation $[a]$ is also used if only one relation.

In other words, if $R$ is an equivalence relation on a set $A$, the equivalence class of the element $a$ is

$$
[a]_{R} = \set{s \mid (a,s) \in R}.
$$

A **representative** of this equivalence class is an element $b$ such that $b \in [a]_{R}$.

### 9.5.3 Equivalence Classes and Partitions

#### Theorem 1

Let $R$ be an *equivalence relation* on a set $A$. These statements for elements $a, b$ of $A$ are equivalent:

$$
\begin{align}
\text{(i)} &\quad aRb \\
\text{(ii)} &\quad [a] = [b] \\
\text{(iii)} &\quad [a] \cap [b] \ne \emptyset \\
\end{align}
$$

**Proof:**

$\text{(i)} \implies \text{(ii)}$: Proof the result by showing that $[a] \subseteq [b]$ and $[b] \subseteq [a]$.

Proof of $[a] \subseteq [b]$: let $c \in [a]$. By definition, $aRc$. Since $aRb$ and $R$ is symmetric, then $bRa$. Furthermore, since $R$ is transitive and $bRa, aRc$, it follows that $bRc$. Hence $c \in [b]$. This shows that $[a] \subseteq [b]$.

Proof of $[b] \subseteq [a]$: let $d \in [b]$. By definition, $bRd$. Since $R$ is transitive and $aRb, bRd$, it follows that $aRd$. Hence $d \in [a]$. This shows that $[b] \subseteq [a]$.

$\text{(ii)} \implies \text{(iii)}$:

Let $[a] = [b]$. Since $R$ is reflexive, then $a \in [a]$ and therefore $[a]$ is nonempty. It follows that $[a] \cap [b] \ne \emptyset$.

$\text{(iii)} \implies \text{(i)}$:

Let $[a] \cap [b] \ne \emptyset$. Then there exists an element $c$ such that $c \in [a]$ and $c \in [b]$. By definition, we have $aRc$ and $bRc$. Since $R$ is symmetric, we have $cRb$. Furthermore, since $R$ is transitive and $aRc, cRb$, it follows that $aRb$.


