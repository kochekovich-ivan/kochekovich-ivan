##  What Is a pandas Series?
- A **1D labeled array** built upon NumPy’s ndarray with an associated **index** (axis labels).  
- Can store **any data type** (numbers, strings, objects, etc.).  
  :contentReference[oaicite:0]{index=0}

---

##  Key Behaviors & Mechanics

###  Element-wise Operations & Index Alignment
- Applying operations (e.g., `+`, `-`, `*`, `/`) on two Series aligns them based on their **indexes**, not positions.  
- The resulting Series has an index that’s the **sorted union** of the two input indexes.  
  :contentReference[oaicite:1]{index=1}

###  NumPy ufuncs Preserve Labels
- Universal functions (like `np.exp`, `np.sin`, etc.) can be used on Series, and they **retain the original index**, making transformations intuitive.  
  :contentReference[oaicite:2]{index=2}

---

##  Summary Table

| Feature                | Description                                                                 |
|------------------------|-----------------------------------------------------------------------------|
| Element-wise operations| Series align by index when performing arithmetic                            |
| Index preservation     | Operations and ufuncs preserve the index of the original Series             |
| Result indexing        | For two Series, result’s index = sorted union of both input indexes         |

---

##  Why It Matters
- **Automatic alignment** prevents errors and simplifies combining data from different sources.
- **Consistent labeling** makes operations predictable and data-aware.
- Enhances safety in analytics workflows compared to raw NumPy arrays or lists.

