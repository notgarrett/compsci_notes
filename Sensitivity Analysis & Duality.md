---
tags:
  - linear_programming
  - mathematics
  - math-3331
---
# Graphical Sensitivity Analysis

**Sensitivity analysis**: Concerned with how changes in an LP's (linear problem's) parameters affect the optimal solution.

```ad-question
How would changes in the problem's object function coefficients or the contraint's right hand sides change this optimal solution?
```

## Example: Giapetto problem

$$\begin{align*}
max(z) &= 3x_{1}+ 2x_{2}\\
2x_{1}+x_{2}&\le 100\\
x_{1}+ x_{2} &\le 80\\
x_{1}&\le 40\\
x_{1},x_{2}&\ge 0
\end{align*}$$

Our optimal solution to this problem was $z = 180, x_{1}=20, x_{2}=60$ and it has $x_{1}, x_{2}, s_{3}$ as basic variables. (s3 is a slack variable for the demand constraint)

If the isoprofit line is flatter than the carpentry constraint, point A(0, 80) is optimal.

