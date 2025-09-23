## Explanation

For a square matrix **A**, an **eigenvector** v and **eigenvalue** λ satisfy:

A × v = λ × v  

Where:  
- v ≠ 0 (non-zero vector)  
- λ is a scalar  

Eigenvectors represent directions that remain unchanged under the transformation A, while eigenvalues represent the scaling factor along those directions.

## Finding Eigenvalues and Eigenvectors

### 1. Eigenvalues
- Solve the **characteristic equation**:

det(A − λI) = 0  

Where I is the identity matrix of the same size as A.

### 2. Eigenvectors
- For each eigenvalue λ, solve:

(A − λI)v = 0  

to find the corresponding eigenvectors.

## Example

Matrix A = [[2, 1], [1, 2]]  

1. Characteristic equation: det([[2−λ, 1], [1, 2−λ]]) = (2−λ)^2 − 1 = 0  
   - λ^2 − 4λ + 3 = 0 → λ = 1, 3  

2. Eigenvectors:
   - λ = 3 → (A − 3I)v = 0 → v = [1, 1]^T  
   - λ = 1 → (A − I)v = 0 → v = [1, −1]^T  

## Properties

- Sum of eigenvalues = trace(A) (sum of diagonal elements)  
- Product of eigenvalues = det(A)  
- Eigenvectors corresponding to distinct eigenvalues are linearly independent  
- For symmetric matrices:
  - Eigenvalues are real  
  - Eigenvectors are orthogonal  

## Applications / Use Cases

- Principal Component Analysis (PCA) in statistics  
- Diagonalization of matrices for simplifying computations  
- Stability analysis in engineering and physics  
- Vibration analysis in mechanical systems  
- Google's PageRank algorithm  
- Quantum mechanics and linear transformations

## Key Points / Notes

- Eigenvalues can be real or complex.  
- Eigenvectors are determined up to a scalar multiple.  
- Diagonalizable matrices have a full set of linearly independent eigenvectors.  
- Finding eigenvalues/eigenvectors is central to solving linear differential equations and transforming systems into simpler forms.  
