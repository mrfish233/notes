# 9 Relations

## 9.1 Relations and Their Properties

### Definition 1 - Binary Relation

Let $A$ and $B$ be sets. A **binary relation** from $A$ to $B$ is a subset of $A \times B$. The notation $aRb$ is used to denote $(a,b) \in R$ and $a \not R b$ is $(a,b) \not \in R$.

### Definition 2 - Relation on a Set

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


