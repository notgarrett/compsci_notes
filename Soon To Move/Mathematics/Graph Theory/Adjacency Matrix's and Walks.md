# Walks

A **walk** is a sequence of vertices and edges, for example: 

$$u_{1},u_{1}u_{2}, u_{2}, u_{2}u_{3}, u_{3}, u_{3}u_{4},u_{4}$$

This is a walk from $u_{1}$ to $u_{4}$.

A[[Graphic Graphs | graph]] is connected if there is a walk between any two vertices.

A **graph** $(V\prime, E\prime)$ is a sub graph of a graph $(V,E)$ if $V\prime \subseteq V, E\prime \subseteq E$

A **sub graph** is said to be a *connected component* of a graph if it is the *maximal* connected sub graph. 

![[SubgraphRepresentation.excalidraw | center]]

The **complement** of a graph $G=(V,E)$ consists of all edges in the complete graph but not in $E$. 

```ad-important
Just to note, this implies that the complement of a complete graph has no edges and is just a bunch of dangling vertices.
```

## Euler Walks

A **Euler walk** is a walk which consists of using all edges exactly once.

A **Hamiltonian walk** is a Euler walk in which you start and end on the same vertex. 


# Adjacency Matrix

