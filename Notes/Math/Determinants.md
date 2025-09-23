## Explanation

A **determinant** is a scalar value derived from a square matrix that provides useful information about the matrix, such as whether it is invertible and the volume scaling factor for linear transformations.

- Denoted as det(A) or |A| for a matrix A.  
- Only defined for **square matrices** (n × n).

## Properties of Determinants

1. **Determinant of 1×1 matrix:**  
   det([a]) = a

2. **Determinant of 2×2 matrix:**  
   det([[a, b], [c, d]]) = ad − bc

3. **Determinant of 3×3 matrix (Rule of Sarrus):**  
   det([[a, b, c], [d, e, f], [g, h, i]]) = aei + bfg + cdh − ceg − bdi − afh

4. **Row/Column Operations:**
   - Swapping two rows/columns multiplies determinant by −1.  
   - Multiplying a row/column by scalar k multiplies determinant by k.  
   - Adding a multiple of one row/column to another does not change determinant.

5. **Triangular Matrices:**  
   - Determinant = product of diagonal elements.

6. **Determinant of Transpose:**  
   - det(A^T) = det(A)

7. **Product Rule:**  
   - det(AB) = det(A) × det(B)

8. **Invertibility:**  
   - Matrix A is invertible ⇔ det(A) ≠ 0

## Methods of Calculation

### 1. Expansion by Minors / Cofactors
- Choose a row or column, multiply each element by its cofactor, sum results.

### 2. Row Reduction
- Transform matrix to upper triangular form, then multiply diagonal elements.

### 3. Special Patterns
- 2×2 or 3×3 matrices can use formulas for quick calculation.

## Examples

- 2×2 matrix: [[3, 2], [1, 4]] → det = 3*4 − 2*1 = 10  
- 3×3 matrix: [[1, 2, 3], [4, 5, 6], [7, 8, 9]] → det = 0  

## Applications / Use Cases

- Solve systems of linear equations (Cramer’s Rule).  
- Determine matrix invertibility.  
- Compute area/volume in geometry using vectors.  
- Find eigenvalues of a matrix.  
- Linear transformations in physics and engineering.

## Key Points / Notes

- Determinants are only defined for **square matrices**.  
- Zero determinant indicates linear dependence among rows or columns.  
- Properties like multilinearity, alternating sign, and multiplicativity simplify calculations.  
