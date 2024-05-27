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

**Proof:**

Let $G = (V,E)$ be an undirected graph with $m$ edges, and let $V_{1}, V_{2}$ be the set of vertices of even degree and the set of vertices of odd degree respectively. Then

$$
2m = \sum\limits_{v \in V} \deg(v) = \sum\limits_{v \in V_{1}} \deg(v) + \sum\limits_{v \in V_{2}} \deg(v)
$$

Since $\deg(v)$ is even for $v \in V_{1}$, then $2m - \sum\limits_{v \in V_{1}} \deg(v)$ is even. And all the terms in $\sum\limits_{v \in V_{2}} \deg(v)$ are odd, there must be an even number of terms. Thus there are an even number of vertices of odd degree.

#### Definition: Adjacent

When $(u,v)$ is an edge of the graph $G$ with *directed edges*, $u$ is said to be **adjacent to** $v$ and $v$ is said to be **adjacent from** $u$.

The vertex $u$ is called the **initial vertex** of $(u,v)$ and $v$ is called the **terminal** or **end vertex** of $(u,v)$.

#### Definition: In-Degree and Out-Degree

In a graph with directed edges, the **in-degree** of a vertex $v$, denoted by $\deg^{-}(v)$, is the number of edges with $v$ as their terminal vertex. The **out-degree** of $v$, denoted by $\deg^{+}(v)$, is the number of edges with $v$ as their initial vertex.

#### Theorem 3

Let $G = (V,E)$ be a graph with directed edges. Then

$$
\sum\limits_{v \in V} \deg^{-}(v) = \sum\limits_{v \in V} \deg^{+}(v) = |E|.
$$

### 10.2.3 Special Simple Graphs

#### Path

A **path** on $n$ vertices, denoted by $P_{n}$, is a simple graph consisting of $n$ vertices which can be labeled by $v_{1}, v_{2}, \cdots, v_{n}$ such that two vertices $v_{i}, v_{j}$ are adjacent if $|i-j| = 1$.

#### Cycle

A **cycle** on $n$ vertices, denoted by $P_{n}$, is a simple graph consisting of $n$ vertices which can be labeled by $v_{1}, v_{2}, \cdots, v_{n}$ such that two vertices $v_{i}, v_{j}$ are adjacent if $|i-j| = 1$ or $n-1$.

#### Complete Graphs

A **complete graph** on $n$ vertices, denoted by $K_{n}$, is a simple graph that contains exactly one edge between each pair of distinct vertices.

![complete_graph](complete-graph.png)

#### n-Cubes

An $n$-dimensional hypercube, or **n-cube**, denoted by $Q_{n}$, is a graph that has vertices representing the $2^{n}$ bit strings of length $n$. Two vertices are adjacent if and only if the bit strings that they represent differ in exactly one bit position.

![n-cubes](n-cubes.png)

### 10.2.4 Bipartite Graphs

#### Definition: Bipartite

A simple graph $G$ is called **bipartite** it its vertex set $V$ can be partitioned into 2 disjoint sets $V_{1}, V_{2}$ such that every edge in the graph connects a vertex in $V_1$ and a vertex in $V_{2}$.

The pair $(V_{1}, V_{2})$ is a **bipartition** of the vertex set $V$ of $G$.

![bipartite](bipartite.png)

#### Theorem 4

A simple graph is **bipartite** if and only if it is possible to assign one of two different colors to each vertex of the graph so that no two adjacent vertices are assigned the same color.

#### Complete Bipartite Graph

A complete bipartite graph $K_{m,n}$ is a graph that has its vertex set partitioned into 2 subsets of $m$ and $n$ vertices, respectively with an edge between 2 vertices if and only if 1 vertex is in the first subset and the other vertex is in the second subset.

![complete-bipartite](complete-bipartite.png)

### 10.2.5 Bipartite Graphs and Matchings

#### Matching

A matching $M$ in a simple graph $G = (V,E)$ is a subset of the set $E$ of edges of the graph such that no two edges are incident with the same vertex.

![[matching.png]]

A matching $M$ in a bipartite graph $G = (V,E)$ with bipartition $(V_{1}, V_{2})$ is a **complete matching** from $V_{1}$ to $V_{2}$ if every vertex in $V_{1}$ is the endpoint of an edge in the matching, or $|M| = |V_{1}|$.

#### Theorem 5: Hall's Marriage Theorem

The bipartite graph $G = (V,E)$ with bipartition $(V_{1}, V_{2})$ has a complete matching from $V_{1}$ to $V_{2}$ if and only if $|N(A)| \ge |A|$ for all subsets $A$ of $V_{1}$.

### 10.2.7 New Graphs from Old

#### Definition: Subgraph

A **subgraph** of a graph $G = (V,E)$ is a graph $H = (W,F)$ where $W \subseteq V$ and $F \subseteq E$. A subgraph $H$ of $G$ is a **proper subgraph** of $G$ if $H \ne G$.

