## 1. Matrix as Transformation
- A matrix represents a linear transformation.  
- Multiplying a matrix by a vector = applying that transformation.

---

## 2. Composition of Transformations
- Matrix multiplication corresponds to doing one transformation after another.  
- If B transforms vector v, and A transforms the result, then:  
  A(Bv) = (AB)v  

---

## 3. Geometric Meaning
- Transformations can be chained:  
  - Example: stretch → rotate → reflect.  
- The product AB is itself a single transformation that captures both steps.

---

## 4. Key Takeaways
- **Matrix multiplication = composition of linear transformations.**  
- **Order matters:** AB ≠ BA in general.  
- Useful for combining effects in graphics, physics, and data science.
