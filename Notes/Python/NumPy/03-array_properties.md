### Array Properties

NumPy arrays have several attributes that describe their characteristics:

- **Shape**: A tuple representing the dimensions of the array.

`arr.shape`

- **Size**: The total number of elements in the array.

`arr.size`

- **Data Type (dtype)**: The type of elements stored in the array.

`arr.dtype`

- **Number of Dimensions (ndim)**: The number of axes (dimensions) the array has.

`arr.ndim`

- **Item Size**: The size (in bytes) of each element in the array.

`arr.itemsize`

- **Flags**: Information about the memory layout and other properties of the array.

`arr.flags`

### Array Representation

Understanding how arrays are represented in memory is essential for optimizing performance:

- **Memory Layout**: NumPy arrays can be stored in either row-major (C-style) or column-major (Fortran-style) order.

  - **C-order**: The last index varies the fastest.
  
`arr = np.array([[1, 2], [3, 4]], order='C')`

  - **F-order**: The first index varies the fastest.
  
`arr = np.array([[1, 2], [3, 4]], order='F')`

- **Contiguous vs. Non-contiguous Arrays**: Contiguous arrays have their elements stored in a single, continuous block of memory, while non-contiguous arrays may have gaps between elements.

`arr = np.array([[1, 2], [3, 4]])`
`arr_transposed = arr.T  # Non-contiguous`

Use the .flags attribute to check if an array is contiguous:

`arr.flags['C_CONTIGUOUS']`

### Copying Arrays

Creating copies of arrays is important to avoid unintended modifications:

- **Shallow Copy**: Creates a new array object, but the data is not copied. Changes to the data will affect both arrays.

`arr_copy = arr.view()`

- **Deep Copy**: Creates a new array object and copies the data. Changes to the data will not affect the original array.

`arr_deep_copy = arr.copy()`

## Key Points / Notes

- Understanding array properties helps in optimizing memory usage and computational efficiency.
- Choosing the appropriate memory layout (C-order vs. F-order) can impact performance, especially for large datasets.
- Be cautious when using shallow copies, as modifications can affect the original array.
