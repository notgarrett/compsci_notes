---
tags:
  - linear_programming
  - math-3331
date: 2024-11-03
---
# Simplex Method Breakdown

**Steps:** 
1. Set constraints into equalities with slack variables.
2. Set Z function to have all variables on the left hand side.
3. Set up simplex tablue.
4. Look for the greatest negative value on the bottom row.
5. Look for the smallest ratio, (b value divided by column value).
6. Do Row reduction.
7. Repeat until all values are positive on the bottom.

## Example:



# Big M Method
**Steps:**
1. Identify minimising problem
2. Set up inequalities into equalities. 


# Two Phase Simplex Method Breakdown

```ad-important
Dual phase is needed when the constraints do not have an obvious feasible solution. You also tend to use this method when you have symbols like $\ge$ in constraints. (As opposed to $\le$ for regular simplex method.)
```

**Steps:**
1. Identify two phase problem.
2. Set constraints to equalities. 
3. $\le$ adds a slack variable, $\ge$ adds a negative slack variable, and a $A_{i}$ variable. $=$ just adds an $A_{i}$ variable.
4. Create a $W'$ function, (Basically all your A variables.)
5. Remove A variables from W function by adding a constraint that would remove them.
6. Solve tablue after initial setup. (Remember W function is a minimizing function)
7. Evaluate Cases
8. Proceed depending on cases.


Case 1: W' is equal to 0.
1. Problem has no feasible solution.

Case 2: All Ai variable is non basic.
1. Remove Ai column(s)
2. Resub Z function into tablue (add a constraint to remove basis variables)
3. Solve.

Case 3: 1 (or more) basic Ai variables.
1. Negative columns are dropped
2. 


