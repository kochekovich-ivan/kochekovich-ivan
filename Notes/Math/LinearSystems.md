## Explanation

A **linear system** is a collection of linear equations involving the same set of variables.  
Each equation is of the form:

a1*x1 + a2*x2 + ... + an*xn = b

Where:  
- x1, x2, ..., xn are **variables**  
- a1, a2, ..., an are **coefficients**  
- b is a **constant term**

Linear systems can have one solution, infinitely many solutions, or no solution.

## Methods of Solving

### 1. Substitution
- Solve one equation for one variable, substitute into other equations.  
- Repeat until all variables are found.

### 2. Elimination
- Add or subtract equations to eliminate one variable.  
- Solve remaining equations step by step.

### 3. Matrix Method (Linear Algebra)
- Represent system as **Ax = b**, where A is the coefficient matrix, x is the variable vector, b is the constants vector.  
- Solve using:
  - **Inverse matrix:** x = A^(-1) * b (if A is invertible)  
  - **Gaussian elimination**  
  - **LU decomposition**  

### 4. Determinants (Cramer’s Rule)
- For n equations with n variables, x_i = det(A_i) / det(A)  
- A_i is formed by replacing the i-th column of A with b.

## Types of Solutions

1. **Unique Solution:** determinant of coefficient matrix ≠ 0.  
2. **No Solution:** inconsistent system.  
3. **Infinitely Many Solutions:** determinant = 0 and system is dependent.

## Example

2x + 3y = 5  
4x − y = 1  

- Solve by elimination: multiply second equation by 3 → 12x − 3y = 3  
- Add to first equation → 14x = 8 → x = 8/14 = 4/7  
- Substitute x → 2*(4/7) + 3y = 5 → y = 13/21

## Applications / Use Cases

- Electrical circuits (Ohm’s and Kirchhoff’s laws).  
- Mechanical systems (forces and equilibrium).  
- Economics (supply-demand balance).  
- Computer graphics and 3D transformations.  
- Solving systems of differential equations in physics and engineering.

## Key Points / Notes

- Linear systems follow the principle of superposition.  
- Consistency and number of solutions can be checked via rank of the matrix.  
- Choosing an appropriate method depends on number of variables, system size, and computational resources.  
