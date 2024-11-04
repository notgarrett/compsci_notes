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


# Dual Phase Simplex Method Breakdown

```ad-important
Dual phase is needed when the constraints do not have an obvious feasible solution. You also tend to use this method when you have symbols like $\ge$ in constraints. (As opposed to $\le$ for regular simplex method.)
```

Case 1: W' is equal to 0.
Problem has no feasible solution.

Case 2: Ai variable is non basic.
Remove Ai column(s)
Resub Z function into tablue
Solve.

Case 3: 

