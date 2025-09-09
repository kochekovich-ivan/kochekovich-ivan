##  What Happens During Operations?
- When performing arithmetic between two Series, pandas **aligns elements by index labels**, not by position.
- If an index is missing in one Series, the result will have `NaN` for that label.
- The resulting Series uses the **union of indexes** from both operands.

## Examples of Operations
- Standard operators (`+`, `-`, `*`, `/`, `**`) work element-wise with automatic alignment.
- Built-in methods and NumPy functions (e.g., `max()`, `mean()`, `np.exp`) work on Series and **preserve index labels**.

##  Why It Matters
- Ensures consistency when combining Series with different indexes.
- Prevents misalignment errors when merging or comparing data.
- Retains label information, making data manipulations intuitive and safe.
