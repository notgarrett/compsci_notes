---
date: 2025-01-21$
tags:
  - computer_graphics
  - linear_algebra
---


# Parametric Equations

Parametric equations have applications in computer graphcis.

Redefine equation in terms of a new parameter.
- Typically called t.
- Define it for curves and lines, $y=f(x)$, $y=mx+b$

Sometimes it is useful to look differently, we define functions as progress along the curve of a line.

![[Parametric Functions Line Example|100%]]

As t goes from 0 to 1, we have two functions that give us x,y.
$x=f_{x}(t)$
$y = f_{y}(t)$

## Parametric Form for Line Segment

$y = mx + b$, Lets parameterise this equation.

$$\begin{align*}
t_{0}&= \text{Start of Segment}\\
t_{1}&= \text{End of Segment}
\end{align*}$$

![[parametric form for line segment example|center]]

$$\begin{align*}
\vec{l} &=  P_{2}-P_{1}\\
\vec{l}(t)&= P_{1}+t*\vec{l}\\
&= <x_{1},y_{1}>+t<x_{2}-x_{1},y_{2}-y_{1}>\\
x &= x_{1}+t(x_{2}-x_{1})\\
y &= y_{1}+t(y_{2}-y_{1}
\end{align*}$$


## Parametric Equations for a Circle

A circle can be defined as the locus of all points that satisfy the equations:
- $x=r\cos{t}$
- $y = r\sin{t}$
- Where x,y are the coordinates of any point of the circle, r is the radius of the circle and t is the parameter.

## Parametric Equations for Lissajous Curve

Lissajour curves are the family of curves described by the parametric equations written in the form:

$$\begin{align*}
x(t) &= a\sin(\omega t+\delta)\\
y(t) &= b\sin(t)
\end{align*}$$

## Parametric Equation of a Sphere

The sphere $x^{2}+y^{2}+z^{2}=r^{2}$ can be parameterised using spherical coordinates:
$$\begin{align*}
x &= r\sin\phi\cos\theta\\
y &= r\sin\phi\cos\theta\\
z &= r\cos\phi\\
0 &\le \theta \le 2\pi, 0\le\phi\le\pi
\end{align*}$$

```ad-tip
Instead of t, we have u and v in a sphere.
$$\begin{align*}
u &= [0...1], v=[0...1]\\
x &= r\sin(\phi u)\cos(\theta v)\\
y &= r\sin(\phi u)\sin(\theta v)\\
z &= r\cos(\phi v)
\end{align*}$$
```


## Lines Intersection using Parametric Equations

If both $t_{a}$ and $t_{b}$ is between \[0...1], we have an intersection.

If $t_{a}[0...1], t_{b}<0$ then $t_{b}$ can hit $t_{a}$ but not in a given line segment, so where is no intersection

![[Lines Intersection using Parametric Equations|center]]

# Line-Line Intersection (2D)

The intersection point of the lines is found with one of the following values of t or u, where:

$$t = \begin{pmatrix}\end{pmatrix}$$