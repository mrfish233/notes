# Graphs

## 10.1 Graphs and Graph Models

#### Definition: Graph

A **graph** $G = (V, E)$ consists of $V$, a nonempty set of *vertices* (or nodes) and $E$, a set of *edges*.

A graph with an infinite vertex set or an infinite number of edges is called an *infinite graph*. A graph with a finite vertex set and a finite edge set is called a *finite graph*.

#### Definition: Directed Graph

A **directed graph** (or digraph) $(V, E)$ consists of a nonempty set of vertices $V$ and a set of **directed edges** (or arcs) $E$. Each directed edge is associated with an ordered pair of vertices. The directed edge associated with the ordered pair $(u,v)$ is said *start at $u$ and end at $v$*.

## 10.2 Graph Terminology

### 10.2.2 Basic Terminology

#### Definition: Adjacent

Two vertices $u$ and $v$ in an undirected graph $G$ are called **adjacent** (or neighbors) in $G$ if $u$ and $v$ are endpoints of an edge $e$ of $G$. Such an edge $e$ is called *incident with* the vertices $u$ and $v$ and $e$ is said to *connect* $u$ and $v$.

#### Definition: Neighborhood

The set of all neighbors of a vertex $v$ of $G = (V, E)$, denoted by $N(v)$, is called the **neighborhood** of $v$.

If $A$ is a subset of $V$, then $N(A)$ is the set of all vertices in $G$ that are *adjacent to* at least one vertex in $A$.

$$
N(A) = \bigcup_{v \in A} N(v).
$$

#### Definition: Degree

The **degree** of a vertex in an *undirected graph* is the number of edges incident with it, except that a loop at a vertex contributes twice to itself. The degree of the vertex $v$ is denoted by $\deg(v)$.

#### Theorem 1: The Handshaking Theorem

Let $G = (V, E)$ be an undirected graph with $m$ edges. Then

$$
2m = \sum\limits_{v \in V} \deg(v).
$$

*Note:* this applies even if multiple edges and loops are present, or the graph is not simple graph.



#### Theorem 2

An undirected graph has an even number of vertices of odd degree.
