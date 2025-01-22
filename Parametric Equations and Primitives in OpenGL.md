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
