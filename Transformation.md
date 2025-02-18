---
date: 2025-02-06
tags:
  - computer_graphics
---
# What is Transformation?

Ideally, we want to make existing code (eg., an object) apply a transformation and draw that.
- We don't want to have to re-create the geometry for each variation.

We need standardised transformations. 
- Rotate
- Scale
- Translate

## Standard Transformation

**Idea:** Do transformation in standard code.
- Translate: $Pt^{\prime} = Pt + offset$
- Scale: $Pt^{\prime} = Pt * x$
- Rotate: etc...

**Problem:** Doesn't scale.
- How do I combine operations? (Just do them in order)
- How do we do the inverse? (work backwards)
- Handle everything separately.

# Idea - Linear Algebra

Already deals with coordinate systems and vector points.

If we represent transformations as matrices things get much easier. 

Two valid systems:
- Points as a new vector.
- Point as a column vector.

**New Vector:**
$$\begin{pmatrix}x & y\end{pmatrix}\begin{pmatrix}M_{1} & M_{2} \\ M_{3} & M_{4}\end{pmatrix}=\begin{pmatrix}x_{T} & y_{T}\end{pmatrix}$$

**Column Vector:** 
$$\begin{pmatrix}M_{1} & M_{2} \\ M_{3} & M_{4}\end{pmatrix}\begin{pmatrix}x \\ y\end{pmatrix}=\begin{pmatrix}x_{T} \\ y_{T}\end{pmatrix}$$


We can combine transformations with pre-computing.

$M_{3}, M_{2}, M_{1}$, corresponding to Translate, Scale, and Rotate.

```ad-tip
title: Order matters.
Our order of M's matters. 
$$M_{c} = M_{3}M_{2}M_{1}$$

Dot product with vertices:
$$M_{c}v = (M_{3}(M_{2}(M_{1}v)))$$

Reverse operations:
$$M^{-1}_{c}(M_{c}v)=v$$

Careful with reverse order:
$$
\begin{align*}
M_{3}M_{2}M_{1}P=P^{\prime}\\
M^{-1}_{1}M^{-1}_{2}M^{-1}_{3}P^{\prime}=P
\end{align*}
$$
```


# Transformations as a Change of Basis

Transforming geometry is just changing the coordinate system.
- Same data (perform transformation)

**Standard Basis:**
$$\begin{align*}
P &= O + BP\\
&= \begin{pmatrix}0\\
0\end{pmatrix} + \begin{pmatrix}1 & 0\\
0 & 1\end{pmatrix}\begin{pmatrix}P_{x}\\
P_{y}\end{pmatrix}
\end{align*}$$
Note that $\begin{pmatrix}1 & 0 \\ 0 & 1\end{pmatrix}$ is the identity matrix.













