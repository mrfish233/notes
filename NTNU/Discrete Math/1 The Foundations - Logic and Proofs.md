## 1.1 Propositional Logic

A **proposition**: a declarative sentence that is either true or false. For example:

- $1+1=2$ is true.
- $2+2=3$ is false.

Propositional variables: true is T and false is F.

### Definition 1 - Negation

Let $p$ be a proposition. The _negation of_ $p$, denoted by $\neg p$ (or $\bar{p}$), is the statement "It is not the case $p$.”

### Definition 2 - Conjunction

Let $p$ and $q$ be propositions. The *conjunction of* $p$ and $q$, denoted by $p \land q$, is the proposition “$p$ and $q$.”

### Definition 3 - Disjunction

Let $p$ and $q$ be propositions. The *disjunction of* $p$ and $q$, denoted by $p \land q$, is the proposition “$p$ or $q$.”

### Definition 4 - Exclusive OR

Let $p$ and $q$ be propositions. The *exclusive or* of $p$ and $q$, denoted by $p \oplus q$, is the proposition when exactly one of $p$ and $q$ is true.

| $p$​ | $q$ | $\lnot p$ | $p \land q$ | $p \lor q$ | $p \oplus q$ |
| ---- | --- | --------- | ----------- | ---------- | ------------ |
| T    | T   | F         | T           | T          | F            |
| T    | F   | F         | F           | T          | T            |
| F    | T   | T         | F           | T          | T            |
| F    | T   | T         | F           | F          | F            |

### Definition 5 - Implication

Let $p$ and $q$ be propositions. The _conditional statement_ $p \to q$ (or $p \Rightarrow q$) is the proposition “if $p$, then $q$.”

The statement $p \to q$ is also called an **implication**. This statement play such an essential role in mathematical reasoning. The following ways will be encountered to express this conditional statement:

- a **sufficient condition** for $q$ is $p$
- a **necessary condition** for $p$ is $q$

**Converse, Contrapositive and Inverse**
The conditional statement $p \to q$ has following related proposition:

- It’s **converse** is $q \to p$.
- It’s **contrapositive** is $\lnot q \to \lnot p$.
- It’s **inverse** is $\lnot p \to \lnot q$.

| $p$ | $q$ | $p \to q$ | $\lnot q \to \lnot p$ | $q \to p$ | $\lnot p \to \lnot q$ |
| --- | --- | --------- | --------------------- | --------- | --------------------- |
| T   | T   | T         | T                     | T         | T                     |
| T   | F   | F         | F                     | T         | T                     |
| F   | T   | T         | T                     | F         | F                     |
| F   | F   | T         | T                     | T         | T                     |

### Definition 6 - Bi-Implications

Let $p$ and $q$ be propositions. The *biconditional statement* $p \leftrightarrow q$ (or $p \Leftrightarrow q$) is the proposition “$p$ if and only if $q$.” Biconditional statements are also called bi-implications.

The other common way to express $p \leftrightarrow q$:

- $p$ iff $q$
- $p$ is necessary and sufficient for $q$

| $p$ | $q$ | $p \to q$ | $p \leftrightarrow q$ |
| --- | --- | --------- | --------------------- |
| T   | T   | T         | T                     |
| T   | F   | F         | F                     |
| F   | T   | T         | F                     |
| F   | F   | T         | T                     |

## 1.3 Propositional Equivalences

### Definition 1

A compound proposition that is always *true* is called a **tautology**.
A compound proposition that is always *false* is called a **contradiction**.
A compound proposition that is *neither* a tautology nor a contradiction is called a **contingency**.

### Definition 2 - Logical Equivalences

The compound propositions $p$ and $q$ are called *logically equivalent* if $p \leftrightarrow q$ is a tautology. The notation $p \equiv q$ denotes that $p$ and $q$ are logically equivalent. The symbol $\Leftrightarrow$ is sometimes used instead of $\equiv$ to denote logical equivalence.

**De Morgan’s Laws**
This truth table shows the equivalence of $\lnot (p \lor q) \equiv \lnot p \land \lnot q$ and $\lnot (p \land q) \equiv \lnot p \lor \lnot q$.

| $p$ | $q$ | $\lnot (p \lor q)$ | $\lnot p \land \lnot q$ | $\lnot (p \land q)$ | $\lnot p \lor \lnot q$ |
| --- | --- | ------------------ | ----------------------- | ------------------- | ---------------------- |
| T   | T   | F                  | F                       | F                   | F                      |
| T   | F   | F                  | F                       | T                   | T                      |
| F   | T   | F                  | F                       | T                   | T                      |
| F   | F   | T                  | T                       | T                   | T                      |

**Conditional-disjunction equivalence**

| $p$ | $q$ | $p \to q$ | $\lnot p \lor q$ |
| --- | --- | --------- | ---------------- |
| T   | T   | T         | T                |
| T   | F   | F         | F                |
| F   | T   | T         | T                |
| F   | F   | T         | T                |

## 1.4 Predicates and Quantifiers

**Predicate** is a sentence that contains a variable. These statements are neither true or false when the values of the variables are not specified.

Let $P(x)$ denote the statement “$x > 3$.” The statement $P(x)$ is said to be the value of the **propositional function** of $P$ at $x$.

**Quantification** is a way to create a proposition from a propositional function.

### Definition 1 - The Universal Quantifier

The *universal quantiﬁcation* of $P(x)$ is the statement “$P(x)$ for all values of $x$ in the domain.” The notation $\forall x \ P(x)$ denotes the universal quantification of $P(x)$. Here $\forall$ is called the **universal quantifier**. We read it as “for all $x P(x)$” or “for every ****$x P(x)$”.

### Definition 2 - The Existential Quantifier

The *existential quantiﬁcation* of $P(x)$ is the statement “There exists an element $x$ in the domain such that $P(x)$.” The notation $\exists x \ P(x)$ denotes the universal quantification of $P(x)$. Here $\exists$ is called the **existential quantifier**.

**Negating Quantified Expressions**

$$
\begin{align}
\lnot \exists x Q(x) \equiv \forall x \lnot Q(x) \\
\\
\lnot \forall x P(x) \equiv \exists x \lnot P(x)
\end{align}
$$

| Negation               | Equivalent Statement   | When is Negation True?                       | When False?                                 |
| ---------------------- | ---------------------- | -------------------------------------------- | ------------------------------------------- |
| $\lnot \exists x P(x)$ | $\forall x \lnot P(x)$ | For every $x$﻿, $P(x)$﻿ is false.            | There is an $x$﻿ for which $P(x)$﻿ is true. |
| $\lnot \forall x P(x)$ | $\exists x \lnot P(x)$ | There is an ﻿$x$ for which $P(x)$﻿ is false. | $P(x)$﻿ is true for every $x$.              |

## 1.5 Nested Quantifiers

Let $Q(x, y)$ denote “$x + y = 0$.” The quantification

$$ \exists y \forall x \ Q(x,y) $$

denotes the proposition “There is real number $y$ such that for every real number $x$, $Q(x, y)$.” The statement is **false** as there’s no real number $y$ such that $x + y = 0$ for all real numbers $x$. The quantification

$$ \forall x \exists y \ Q(x,y) $$

denotes the proposition “For every real number $x$ there is a real number $y$ such that $Q(x, y)$.” The statement is **true** as given a real number $x$, there’s a real number $y$ such that $x + y = 0$.

This illustrates that the **order** in which quantifiers appear makes a difference.

| Statement                      | When True?                                                | When False?                                                |
| ------------------------------ | --------------------------------------------------------- | ---------------------------------------------------------- |
| $\forall x \exists y \ P(x,y)$ | $P(x, y)$ is true for every pair $x$ and $y$.             | There’s a pair$x, y$ for which $P(x, y)$ is false.         |
| $\forall x \exists y \ P(x,y)$ | For every$x$ there is a $y$ for which $P(x, y)$ is true.  | There is an$x$ such that $P(x, y)$ is false for every $y$. |
| $\exists x \forall y \ P(x,y)$ | There is an$x$ for which $P(x, y)$ is true for every $y$. | For every$x$ there is a $y$ for which $P(x, y)$ is false.  |
| $\exists x \exists y \ P(x,y)$ | There’s a pair$x, y$ for which $P(x, y)$ is true.         | $P(x, y)$ is false for every pair $x, y$.                  |

## 1.7 Introduction to Proofs

| Keyword                  | Description                                                                     |
| ------------------------ | ------------------------------------------------------------------------------- |
| theorem (facts, results) | A statement that can be shown to be true.                                       |
| proposition              | A less important theorem.                                                       |
| proof                    | A valid argument that establishes the truth of theorem.                         |
| axioms (postulates)      | Statements we assume to be true.                                                |
| lemma                    | A less important theorem that is helpful in the proof of other results.         |
| corollary                | A theorem that can be established directly from a theorem that has been proved. |
| conjecture               | A statement that is being proposed to be a true statement.                      |

**Methods of Proving Theorems**

1. Direct Proofs
2. Proofs by Contraposition
3. Proofs by Contradiction

### Direct Proofs

A direct proof shows that a conditional statement $p \to q$ is true by showing that if $p$ is true, then $q$ must also be true.

### Proofs by Contraposition

The conditional statement $p \to q$ can be proved by showing that its contrapositive, $\lnot q \to \lnot p$ is **true**.

**Example:** Let $n$ be an integer. Show that if $n^2$ is odd, then $n$ is also odd.

**Proof**: the contrapositive of the statement is “if $n$ is even, then $n^2$ is also even.” Therefore let $n$ be an even number, $n = 2k$ for some integer $k$. Then

$$ n^2 = (2k)^2 = 4k^2 = 2(2k^2) $$

This shows that $n^2$ is also even. Therefore the statement “if $n^2$ is an odd number, then $n$ is also an odd number” is proved by contraposition.

### Proofs by Contradiction

As the statement $r \land \lnot r$ is a contradiction whenever $r$ is a proposition, we can prove that $p$ is true if we can show that $p \to (r \land \lnot r)$ is true for some proposition $r$.

**Example:** Prove that $\sqrt{2}$ is irrational.

**Proof**: Suppose $\sqrt{2}$ is rational, then there exists integers $a$ and $b \ (b \ne 0)$ such that

$$ \sqrt{2} = \frac{a}{b} $$

We may assume that $\gcd (a, b)$ is equal to $1$ (they have no common factors). (Using the fact that every rational number can be written in lowest terms.) Squaring both side of equations, we have

$$ \begin{aligned} 2 &= \frac{a^2}{b^2} \\ a^2 &= 2b^2 \end{aligned} $$

This shows that $a$ is even. This shows that there exists an integer $c$ such that $a = 2c$. Then

$$ \begin{aligned} 2b^2 &= a^2 \\ &= (2c)^2 \\ &= 4c^2 \\ b^2 &= 2c^2 \end{aligned} $$

This shows that $b$ is even. As both $a$ and $b$ is even, $\gcd (a,b)$ must be greater than $2$. This contradicts with our assumption of $\gcd (a,b) = 1$. Therefore $\sqrt{2}$ is rational is false and we have proved that $\sqrt{2}$ is irrational.

## 1.8 Proof Methods and Strategy

### Existence Proofs

A theorem of this type is a proposition of the form $\exists x P(x)$, where $P$ is predicate. Several ways to prove a theorem of this type:

- **Constructive Existence Proof:** proof by finding an element $a$, called a **witness**, such that $P(a)$ is true.
- **Nonconstructive Existence Proof**: proof by other ways rather than finding $a$.

### Uniqueness Proofs

These theorems assert that there is exactly one element with this property. The two parts of a uniqueness proof are:  

- **Existence**: show that an element $x$ with the desired property exists.
- **Uniqueness**: show that if $x$ and $y$ both have the desired property, then $x=y$.