## Explanation

The **inverse of a matrix** A is another matrix A^(-1) such that:

A × A^(-1) = A^(-1) × A = I  

Where **I** is the identity matrix of the same size.  
- Only **square matrices** can have inverses.  
- A matrix is **invertible** (non-singular) if det(A) ≠ 0.  

## Properties of Matrix Inverses

1. (A^(-1))^(-1) = A  
2. (AB)^(-1) = B^(-1) × A^(-1)  
3. (A^T)^(-1) = (A^(-1))^T  
4. (kA)^(-1) = (1/k) A^(-1), k ≠ 0  
5. det(A^(-1)) = 1 / det(A)

## Methods to Find Inverse

### 1. For 2×2 Matrix
A = [[a, b], [c, d]]  

If det(A) ≠ 0, then  

A^(-1) = (1 / det(A)) * [[d, -b], [-c, a]]  

### 2. Using Adjoint / Cofactor Method
- Compute matrix of cofactors.  
- Transpose cofactor matrix → adjoint.  
- Multiply by 1/det(A): A^(-1) = adj(A) / det(A)

### 3. Using Row Reduction (Gauss-Jordan)
- Augment matrix A with identity I: [A | I]  
- Apply row operations to transform A → I  
- Resulting right-hand side becomes A^(-1)

### 4. Using Elementary Matrices
- Express A as product of elementary matrices: A = E1 × E2 × ... × En  
- Then A^(-1) = En^(-1) × ... × E2^(-1) × E1^(-1)

## Example

2×2 matrix: A = [[2, 3], [1, 4]]  
- det(A) = 2*4 − 3*1 = 5  
- A^(-1) = (1/5) * [[4, -3], [-1, 2]]  

## Applications / Use Cases

- Solve systems of linear equations: x = A^(-1) * b  
- Computer graphics (transformations, rotations, scaling)  
- Control systems and signal processing  
- Matrix decomposition and optimization problems  
- Economics and physics modeling

## Key Points / Notes

- Not all matrices have inverses; det(A) = 0 → singular matrix.  
- Inverse exists only for square matrices.  
- Avoid computing inverses manually for large matrices; use software or numerical methods.  
- In solving Ax = b, using A^(-1) is conceptually useful but computationally expensive for large systems.  
