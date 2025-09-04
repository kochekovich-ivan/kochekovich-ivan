## Matrices

### Definition

A matrix is a **rectangular array of numbers** arranged in rows and columns.

Example of a 2x3 matrix:

[ a11 a12 a13 ]
[ a21 a22 a23 ]


### Matrix Addition

- Only possible if matrices have the **same shape**.
- Add corresponding elements.

[1 2] [5 6] [6 8]
[3 4] + [7 8] = [10 12]


### Scalar Multiplication

- Multiply every element by a scalar.

2 * [1 2] = [2 4]
[3 4] [6 8]


### Matrix Multiplication

- Number of **columns of first matrix** = number of **rows of second matrix**.
- Multiply rows by columns (dot product).

[1 2] [5 6 7] [15+28 16+29 17+210]
[3 4] * [8 9 10] = [35+48 36+49 37+410]


### Special Matrices

- **Zero matrix**: all entries are 0
- **Identity matrix**: square matrix with 1's on the diagonal, 0's elsewhere

[1 0 0]
[0 1 0]
[0 0 1]


### Transpose

- Flips a matrix over its diagonal (rows become columns)

[1 2 3]ᵀ = [1 0]
[0 4 5] [2 4]
[3 5]
