## 1. Inverse Matrix
- **Definition:** For a square matrix A, the inverse A⁻¹ satisfies A⁻¹·A = I.  
- **Condition:** Exists only if det(A) ≠ 0.  
- **Meaning:** If A·x = b, then x = A⁻¹·b.  

---

## 2. Column Space (Image)
- **Definition:** The span of the columns of A.  
- **Interpretation:** All possible outputs of the transformation A·x.  
- **Dimension:** Rank of A.  

---

## 3. Null Space (Kernel)
- **Definition:** The set of all x such that A·x = 0.  
- **Interpretation:** Inputs that collapse to the zero vector.  
- **Dimension:** Nullity of A.  

---

## 4. Connections
- If A is invertible → column space = whole space, null space = {0}.  
- If det(A) = 0 → transformation squashes space (non-trivial null space).  
- **Rank–Nullity Theorem:**  
  dimension(domain) = rank + nullity.  

---

## Summary Table

| Concept         | Definition                          | Geometric Meaning                          |
|-----------------|-------------------------------------|--------------------------------------------|
| Inverse Matrix  | A⁻¹·A = I (det ≠ 0)                | Undo the transformation                    |
| Column Space    | Span of columns of A               | All reachable outputs                      |
| Null Space      | Solutions of A·x = 0               | Inputs that map to zero                    |



