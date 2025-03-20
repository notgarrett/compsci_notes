# Graphic Sequence

A sequence $d_{1},d_{2},...,d_{n}$ is said to be graphic (or, graphical) if there is a (simple) graph such that the degrees of $n$ vertices are exactly $d_{1},d_{2},...,d_{n}$


```ad-question
title: Question
Is 3,2,2,4 graphic? 

More clearly, is there a grapgh with 4 vertices with the degrees 3,2,2,4
```

For a graph with $|V| = 4$, the largest *possible* degree is $4-1 = 3$
# Theorem

Let $G = (V,E)$ be a graph. Then $\sum\limits_{v\in{V}}=2|E|$ 

Furthermore, there are a even number of vertices with odd degrees.

**Proof:** Each edge $uv$ contributes 1 in deg(u), and 1 in deg(v)

$$2|E| = \sum\limits_{v\in{V}}deg(v)$$

```ad-tip
$\sum\limits_{v\in{V}}deg(v)$ is an even number.
```

$$(1.)\sum\limits_{v\in{V}}deg(v) = (2.)\sum\limits_{v\in{V}}deg(v) + (3.) \sum\limits_{v\in{V}}deg(v) $$

(1.): Our value is even.
(2.): Our $deg(v)$ is even. Our summation is even.
(3.): Our $deg(v)$ is odd. Even number of odd degrees.

### Examples

```ad-question
title: Example1
Is 3,2,1,2,3,2 graphic?
```

It is not graphic. This is because their are 3 vertices with odd degrees, or, the sum is odd.

# Havel-Hakimi Theorem

The best way I can describe this **algorithm** is that you take the biggest edge count (of some vertex). 

Like the first 4 in the example: 4,4,4,4,2,1,1

Here, we disperse, or connect, the 4 edges to 4 other edges.

Visualise it like this:

(4-4),(4-1),(4-1),(4-1),(2-1),1,1

Where we are deleting our first 4, and removing a total of 4 edges amongst the other vertices.

Now we have: 3,3,3,1,1,1

Disperse the 3:

2,2,0,1,1 (We do not need to worry about the 0's)

Continue the algorithm:

1,0,0,1

0,0,0,0

Since all our edges sort out, and we have no extra edges, the graph is graphic. 

![[HakimiVisualization.excalidraw | center]]

