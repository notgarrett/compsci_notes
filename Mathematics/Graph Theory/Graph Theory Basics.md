**Definition:** A graph $G=(V,E)$ consists of two sets. The set $V$ is a finite set of vertices. The set $E$ is a finite set of edges.

Each edge is an unordered pair of two vertices.
$$\{u,v\} = uv = \{v,y\} = vu, \ \ u,v\in V$$

![[BasicGraph1.excalidraw | center]]


**Multi graph:** There is at least one multi edge. There are no loops.

**Loops:** A loop is an edge such that the edge is: $uu, \ u\in{V}$

```ad-note
title: Adjecency
Note that $u$ and $v$ are adjacent if $uv \in E$
```

**Complete graph:** $G = {V,E}$ such that $u~v, \forall{u,v} \in V$. This means that for every two vertices in G, there is an edge connecting them.

**Simple graph:** No multi edges, no loops. 

**Pseudo graph:** Multi edges, loops.

```ad-question
title: How many edges can there be in a graph: Kn? 

```

Our answer is: $$|E| = \begin{pmatrix}n\\2\end{pmatrix}$$
Where $n = |v|$