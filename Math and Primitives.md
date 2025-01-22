---
date: 2025-01-14$
tags:
  - computer_graphics
  - linear_algebra
---
# Linear Algebra Review

**Point:** A location in a coordinate system relative to the origin.

**Vector:** A directional quantity (Magnitude and direction)

$$\vec{a} = \vec{b} = \vec{c}$$
$$a \not= b \not= c$$

- Vector \* Scalar = Vector
- Vector + Scalar = Vector
- Point + Vector = Point
- Point - Point = Vector

**Convert a point to a vector:**
$$point - <0,0> = \vec{point}$$

**Euclidean Length of a vector:**
$$|\vec{V}| = \sqrt{Vx^{2}+Vy^{2}+...}$$

**Normalised Vector:** Also known as the unit vector.
$$\hat{v}=\frac{\vec{v}}{{|\vec{v}|}}, |\hat{v}| = 1$$

**Dot Product of Vectors:**
$$\vec{P} * \vec{Q} = |\vec{P}| * |\vec{Q}| * cos(\alpha)$$

If the dot product is 0, Q and P are orthogonal.

If $cos(\alpha)$ = 0, Q and P are co directional.

Slow calculations. 

**Dot Product Better way:**

$$
\begin{align*}
C^{2}&= a^{2}+b^{2}+2ab\cos(\alpha)\\
|P-Q|^{2}&= |\vec{P}|^{2}+|\vec{Q}|^{2}+2|P||Q|\cos(\alpha)\\
\vec{P}*\vec{Q}&= PxQx+PyQy+...\\
&= \sum\limits^{n}_{i=1}P_{i}Q_{i}
\end{align*}
$$


**Cross Product of Vectors:**
$$\vec{P} \times \vec{Q} = |\vec{P}||\vec{Q}|sin(\alpha)*n$$

Where n is the unit vector orthogonal to both P and Q.

If P and Q are co directional or opposite, results in a zero vector.

If P and Q are orthogonal, then the result is a product of vector length. 

Expensive to calculate.