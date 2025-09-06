## 1. Core Idea
- The determinant measures how a linear transformation **scales area (2D)** or **volume (3D+)**.  
- Example: If a unit square is transformed into a parallelogram of area 5 → det = 5.

---

## 2. Sign of Determinant
- **Positive:** Orientation preserved.  
- **Negative:** Orientation flipped (mirror image).  
- **Zero:** Transformation collapses space into lower dimension (area/volume = 0).

---

## 3. 2D Formula
For matrix  
\[
\begin{pmatrix} a & b \\ c & d \end{pmatrix}
\]  
determinant = **ad − bc**.  
Represents the signed area of the parallelogram formed by its column vectors.

---

## 4. Key Properties
- det(AB) = det(A) · det(B)  
- det(I) = 1 (identity preserves space)  
- If det = 0 → matrix is singular (no inverse)

---

## 5. Why It Matters
- Links algebra (matrix operations) with geometry (area/volume).  
- Determines invertibility of a matrix.  
- Used in solving linear systems, computer graphics, physics, and more.
