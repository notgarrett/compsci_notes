---
date: 2025-02-11
tags:
  - computer_graphics
---
# Standard used Patterns

Draw your object in standard object coordinate system.

First draw your object in standard coordinate system and then rely on transformations.

When you transform, then transform all the vertices in a shape uniformly.

For example: If we rotate an object than we rotate all vertices of it to get the effect of rotation. 

If you want to perform rotations:
- You first translate to origin, then rotate, scale, ...
- You then translate it back

# Composing Transformation

Given transformation matrices $M_{1},M_{2},M_{3}...$
$$P^{\prime}= ...M_{3}M_{2}M_{1}P$$

Can calculate:
$$M_{3}M_{2}M_{1}=M$$

```ad-missing
Please review the diagram(s) below and update it accordingly.
```

and apply M to many points; e.g.
$$\begin{pmatrix}s_{x} & 0 & 0 \\ 0 & s_{y} & 0 \\ 0 & 0 & 1\end{pmatrix}\begin{pmatrix}cos\theta  & -sin\theta & 0 \\ sin\theta & cos\theta & 0 \\ 0 & 0 & 1\end{pmatrix}\begin{pmatrix}1 & 0 & t_{x} \\ 0 & 1 & t_{y} \\ 0 & 0 & 1\end{pmatrix}=\begin{pmatrix}...\end{pmatrix}$$


We can undo a transformation using the inverse.
$$MP = P^{\prime}, \ \ \ M^{-1}P^{\prime}=P, \ \ \ M^{-1}(MP) = P$$

Inversion can be slow, but there are tricks to make it faster.

Each transformation has an inverse:
$$\begin{align*}
T^{-1}(t_{x},t_{y})=T(-t_{x},-t_{y})\\
\end{align*}$$

# Transformation Pipeline
*From object space to raster space*

```ad-tip
This pipeline is TOTALLY going to be on the exam. 
```

```ad-warning
Add a pipeline diagram here from the note.
```

**Model Matrix:** Transform from object coordinates to world coordinates
- Set up your model in the world
- Each model has different matrix (multiple model per object)
- Most of your work goes here

**View Matrix:** Transform from the world coordinates to our view camera.
- Use to move a camera/view around without worrying about object location(s).

**Project Matrix:** It handles the transition from virtual (3d) to screen, 2d flat space.
- Transforms from view coordinates to screen coordinates
	- Normalised device coordinates (**NDC**)
	- Extra stuff happens here

**Viewport Transform:** Convert from NDC to raster coordinates.
- Device coordinates
- Often setup by a toolkit

# View Matrix (Camera Model)

Can use existing transformations (TRS).
- This moves the world points, not the camera points (multiple order)

**Camera model:** Construct a basis to move point in and out of camera space. 
- Y: Up, doesn't have to be axis aligned
- X: Perpendicular, some perpendicular vectors




