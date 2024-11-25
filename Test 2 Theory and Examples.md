## 4.13 Two-Phase simplex
1. First, make sure all RHS of constraints are non-negative. Multiply $-1$ through if needed to make RHS non-negative.
2. Make note of any constraint that is an $=$ or $\geq$ constraint.
3. Convert to standard form using slack and excess variables
4. Any constraint noted in step 2 should add an artificial variable $a_{i}\geq{0}$.
5. Ignore original LP's objective function (z function) and **solve** $min\ w^`= \text{sum of all artificial (a) variables}$
6. You'll get 1 of 3 cases:
	1. Optimal value of $w^`$ is greater than zero. NO FEASIBLE SOLUTION.
	2. Optimal value of $w^`$ is equal to zero, and **no artificial (a) variables are in the optimal basis**. In this case, drop all artificial columns, replace the $w^`$ row with the original $z$ row, and solve.
	3. Optimal value of $w^`$ is equal to zero, and **one or more artificial variables are in the optimal basis**. In this case, drop all **nonbasic** artificial columns and **any variable from the original problem that has a negative coefficient in the $z$ row** and solve.
- Examples on page 184 of textbook

## 4.14 URS Variables
- If $x_{i}$ is urs (unrestricted in sign), set $x_{i}=x_{i}^`-x_{i}^{``}$ and $x_{i}^`,x_{i}^{``}\geq 0$. This will make the simplex table have columns for the new variables. 
- Solve the LP using simplex method, and you'll get that either $x_{i}^`$ or $x_{i}^{``}$ is equal to zero, or both are. To find $x_{i}$, simply plug in $x_{i}=x_{i}^`-x_{i}^{``}$.
- Examples on page 189 of textbook

<div style="page-break-after: always;"></div>

## 6.3 $C_{BV},B^{-1},etc$
- $C_{BV}=[C_{BV_{1}},\dots,C_{BV_{n}}]$ (a $1\times n$ matrix)
	- the objective function coefficients for the optimal tableau’s basic variables
- $B$ is the matrix of columns from the **original** LP that correspond to basic variables in the **optimal solution**.
	- Find $B^{-1}$ using standard methods.
	- $B^{-1}$ can also be thought of as simply the **initial tableau's** basic variables' columns in the optimal tableau (but I recommend finding it anyway)
- $b$ is the RHS column of the **original LP, excluding the z row**.
- $A$ is the columns of the **original LP, excluding the z row**.
	- $A_{i}$ is the column pertaining to $x_{i}$
- $C$ is the coefficients in the original $z$ row
	- $c_{i}$ is the coefficient of $x_{i}$ in original $z$ row
- Examples on page 288 of textbook

#### Theory
- $x_{j}$ column in optimal tableau's constraints $= B^{-1}a_{j}$
- RHS of optimal tableau's constraints $=B^{-1}b$
- RHS of optimal tableau's row 0 (z row) $=C_{BV}B^{-1}b$
- Coefficient of $s_{i}$ in optimal row 0 $= i\text{th element of }C_{BV}B^{-1}$
- Coefficient of $e_{i}$ in optimal row 0 $= -(i\text{th element of }C_{BV}B^{-1})$
- Coefficient of artificial $a_{i}$ in optimal row 0 $= i\text{th element of }C_{BV}B^{-1} + M$
	- Specifically for max problem

- new coefficient of $x_{j}$ in optimal tableau: $\overline{x_{j}}=C_{BV}B^{-1}A_{j}-c_{j}$
	- Where $c_{j}$ is the coefficient of $x_{j}$ in the initial z row
	- If $\overline{x_{j}}\geq 0$, current basis remains optimal. Otherwise, enter $x_{j}$ into basis
- When NBV coefficient changes, find $\overline{x_{j}}$
- When BV coefficient changes, entire $z$ row changes.
	- New $z$ row can be found using $C_{BV}B^{-1}A-C$
	- New $z$ row must all be $\geq 0$ to remain optimal
- Changing RHS of a constraint
	- Use the fact that RHS of optimal tableau is $B^{-1}b$
		- These must be $\geq 0$ to remain optimal
	- Optimal $z$ value $=C_{BV}B^{-1}b$

## 6.5 Dual of an LP
- "Normal" max problem
	- All variables are non-negative
	- All constraints are $\leq$
- "Normal" min problem
	- All variables are non-negative
	- All constraints are $\geq$
- Dual of a normal problem is basically a transpose
- Examples on page 301 of textbook

#### Dual of a non-normal max LP
- If the $i$th constraint is $\geq$, the corresponding dual variable $y_{i} \leq 0$
- If the $i$th constraint it $=$, the dual variable $y_{i}$ is urs
- If the $i$th primal variable is urs, the $i$th dual constraint will now be an $=$ constraint

#### Dual of a non-normal min LP
- If the $i$th constraint is $\leq$, the corresponding dual variable $x_{i} \leq 0$
- If the $i$th constraint it $=$, the dual variable $x_{i}$ is urs
- If the $i$th primal variable is urs, the $i$th dual constraint will now be an $=$ constraint

<div style="page-break-after: always;"></div>

## 6.7 The Dual Theorem
- If the primal is unbounded, the dual is infeasible and vice versa
- The optimal value of the primal $z$ is equal to the optimal value of the dual $w$

![[Pasted image 20241106083052.png]]

![[Pasted image 20241106083120.png]]
- Examples on page 313 of textbook
## 6.10 Complementary Slackness
- Assume LP is normal

- $i$th primal slack $> 0$ implies $i$th dual variable $= 0$
- $i$th dual variable $> 0$ implies $i$th primal slack $= 0$

- $j$th dual excess $> 0$ implies $j$th primal variable $= 0$
- $j$th primal variable $> 0$ implies $j$th dual excess $= 0$

- Examples on page 328 of textbook

## 6.11 Dual Simplex Method
- Ensure the LP is normal. Multiply any rows by $-1$ if needed.
- Solve a normal min problem by converting to a max problem
	- Multiply $z$ row by $-1$ and maximize $-z$

1. If the RHS of each constraint is non-negative, current solution is optimal. If not, continue
2. Choose the most negative BV to leave the basis. The row in which the variable is basic is now the pivot **row**. To select the entering variable, we compute the following ratio for each variable $x_{j}$ that has a *negative* coefficient in the pivot row:
	1. $\frac{\text{coefficient of } x_{j} \text{ in row 0}}{\text{coefficient of }x_{j}\text{ in pivot row}}$
	2. Choose the variable with the **smallest absolute value** in the ratio test to enter the basis. Use row operations to make variable basic.
3. If there is any constraint in which the right-hand side is negative and each variable has a non-negative coefficient, then the LP has no feasible solution. If no constraint indicating infeasibility is found, return to step 1.

- Examples on page 335 of textbook

#### Finding the new optimal solution after a constraint is added
- 3 cases:
	- Case 1: The current optimal solution satisfies the new constraint
		- Check this by inputting current optimal x values into constraint
	- Case 2: The current optimal solution does not satisfy the new constraint, but the LP still has a feasible solution
		- Eliminate any BVs from the new row and see if it is possible to satisfy. If it is, continue with dual simplex
	- Case 3: The additional constraint makes the LP have no feasible solution
		- Eliminate any BVs from the new row and see if it is impossible to satisfy.

<div style="page-break-after: always;"></div>

#### Changing RHS of a constraint
- If current optimal solution becomes infeasible, just use dual simplex to solve for new optimal tableau


**Dual simplex is always minimising always.**
$$min(abs(\frac{R_{0}}{R_{p}}))$$