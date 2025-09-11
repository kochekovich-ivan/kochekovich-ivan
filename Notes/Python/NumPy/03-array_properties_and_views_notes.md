## Array Properties

- **dtype** — data type of elements (e.g. float64, int32).  
- **shape** — tuple of dimensions of the array.  
- **ndim** — number of axes (dimensions).  
- **size** — total number of elements in the array.  
- **itemsize** — size in bytes of each element.  
- **nbytes** — total memory consumption (size * itemsize).

## Views and Representations

- Some operations do not copy data, they create new *views* or different *representations* of the same data.  
- Examples of changing representation without copying:
  - changing `shape` attribute  
  - using `reshape()` when possible  
  - transposing with `.T`  
- Views share the same data buffer; modifying data via one view affects all views.

## Creating Copies

- To create an independent copy of array data use `copy()` method.  
- Using `np.array(a, copy=True)` also makes a copy.  
- Assigning by `b = a` does **not** copy: both variables refer to same array/data.

## Why It Matters

- Understanding views vs copies helps avoid unexpected behavior (e.g., unexpected data changes).  
- Saves memory: using views avoids unnecessary duplication.  
- Ensures safe use when you need isolation (copies) vs efficiency (views).
