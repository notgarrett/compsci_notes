---
date: 2025-05-14
tags:
  - linear_algebra
---
[[|Next]]

**Definition:** A *vector space*, or linear space, $V$ over a field $F$ consists of a set on which two operations (addition and scalar multiplication) are defined so that for each pair of elements $x, y \in V$ there is a unique element $x + y \in V$, and for each element $a \in F$ and each element $x \in V$ there is a unique element $ax \in V$, such that the following conditions hold.

1. For all $x, y \in V, x + y = y + x$ (commutativity of addition)
2. For all $x, y, z \in V, (x+y) + z = x + (y + z)$ (Associativity of addition)
3. There exists an element in $V$ denoted by $0$ such that $x + 0 = x$ for each $x \in V$
4. For each element $x \in V$ there exists an element $y \in V$ such that $x + y = 0$
5. For each element $x \in V, 1x = x$
6. For each pair of elements $a, b \in F$ and each element $x \in V, (ab)x = a(bx)$
7. For each element $a \in F$ and each element $x, y \in V, a(x+y) = ax+ay$
8. For each pair of element $a,b \in F$ and each element $x \in V, (a+b)x = ax+bx$


```ad-note
The elements $x+y$ and $ax$ are called the **sum** of $x$ and $y$ and the **product** of $a$ and $x$.
```


An object of the form $(a_{1},a_{2},...,a_{n})$, where the entries $a_{1},...,a_{n}$ are elements of a field $F$, is called an **n-tuple** with entries from $F$. The elements $a_{1},...,a_{n}$ are called the **entries** or **components** of the n-tuple. Two n-tuples $(a_{1},a_{2},...,a_{n}) \text{ and } (b_{1},b_{2},...,b_{n})$ with entries form a field $F$ are called **equal** if $a_{i}=b_{i}$, for $i = 1,2,...,n$.

## Example 1

The set of all n-tuples with entries from a field $F$ is denoted by $F^{n}$. This set is a vector space over $F$ with operations of coordinate-wise addition and scalar multiplication: that is, if $u = (a_{1},a_{2},...,a_{n}) \in F^{n}, v=(b_{1},b_{2},...,b_{n}) \in F^{n}$ and $v\in F$, then:
$$u + v = (a_{1}+ b_{1},a_{2}+b_{2},...,a_{n}+b_{n})$$
Thus $R^{3}$ is a vector space over $R$. In this vector space:
$$(3,-2,0) + (-1,1,4) = (2,-1,4), \text{ and } -5(1,-2,0) = (-5,10,0)$$
Similarly, $C^{2}$ is a vector space over $C$, and has these same properties.

```ad-tip
Vectors in $F^{n}$ may be written as **column vectors:
$$\begin{pmatrix}a_{1} \\ a_{2} \\ ... \\ a_{n}\end{pmatrix}$$ rather than row vectors.
```
A $m\times n$ **matrix** with entries from a field $F$ is a rectangular array of the form

$$\begin{pmatrix}a_{11} & a_{12} & ... & a_{1n} \\ a_{21} & a_{22} & ... & a_{2n} \\ \vdots & \vdots &  & \vdots \\ a_{m1} & a_{m2} & ... & a_{mn}\end{pmatrix}$$
 
where each entry $a_{ij}$ $(1 \le i \le m, 1 \le j \le n)$ is an element of $F$. We call the entires $a_{ij}$ with $i=j$ the **diagonal entries** of a matrix. The entries $a_{i1},a_{i2},...,a_{in}$ compose the **$i^{th}$ row** of the matrix, and the entries $a_{1j},a_{2j},...,a_{nj}$ compose  the **$j^{th}$ column** of the matrix. The rows of the preceding matrix are regarded as vectors in $F^{n}$, and the columns are regarded as vectors in $F^{m}$. The $m \times n$ matrix in which each entry equals zero is called the **zero matrix** and is denoted by $0$. 

## Example 2

