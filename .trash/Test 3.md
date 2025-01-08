## 6.11 Dual Simplex Method
- Ensure the LP is normal. Multiply any rows by $-1$ if needed.
- Solve a normal min problem by converting to a max problem
	- Multiply $z$ row by $-1$ and maximize $-z$

1. If the RHS of each constraint is non-negative, current solution is optimal. If not, continue
2. Choose the most negative BV to leave the basis. The row in which the variable is basic is now the pivot **row**. To select the entering variable, we compute the following ratio for each variable $x_{j}$ that has a *negative* coefficient in the pivot row:
	1. $\frac{\text{coefficient of } x_{j} \text{ in row 0}}{\text{coefficient of }x_{j}\text{ in pivot row}}$
	2. Choose the variable with the **smallest absolute value** in the ratio test to enter the basis. Use row operations to make variable basic.
3. If there is any constraint in which the right-hand side is negative and each variable has a non-negative coefficient, then the LP has no feasible solution. If no constraint indicating infeasibility is found, return to step 1.

<div style="page-break-after: always;"></div>

## 9.3 Branch and Bound
- If $x_{i}$ is not an integer in the optimal solution (PULP to find this), branch on $x_{i}$
	- If there are multiple non-integers that need to be integers, arbitrarily pick one (NOT both)
- Stop at infeasible or integer solutions
- Explore entire tree and pick best option
	- AB prune if you want

![[Pasted image 20241124210116.png|400]]

## 9.7 Implicit Enumeration
1. Test the absolute best case (values of every $x_{i}$ that make z large/small) against all constraints at current node. If feasible, you're done at this node. If infeasible:
2. Test absolute best case for fulfilling each constraint. If you cannot fulfill a constraint, this node is infeasible. If you can fulfill all constraints, branch arbitrarily off of one of the remaining $x_{i}$.
3. Explore entire tree and pick best feasible $z$ value.
	1. AB prune if you wanna be fancy

<div style="page-break-after: always;"></div>

## 9.8 The Cutting Plane Algorithm
![[Pasted image 20241124205814.png]]

#### Notes
- A cut is a constraint to be added to the optimal tableau
- Don't forget to convert to standard form in the new constraint
	- All added cuts add a row and a column