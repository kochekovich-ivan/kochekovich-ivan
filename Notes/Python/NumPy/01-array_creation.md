### Creating Arrays

To create a NumPy array, first import the NumPy library:

`import numpy as np`

Then, use the `np.array()` function to create an array:

`arr = np.array([1, 2, 3, 4, 5])`

This creates a one-dimensional array. You can also create multi-dimensional arrays:

`arr_2d = np.array([[1, 2, 3], [4, 5, 6]])`

This creates a two-dimensional array.

### Data Types

NumPy automatically infers the data type of the array elements. You can specify the data type using the `dtype` parameter:

`arr_float = np.array([1, 2, 3], dtype=float)`

This creates an array with float data type.

## Examples

`import numpy as np`

`# Creating a 1D array`
`arr = np.array([1, 2, 3, 4, 5])`
`print(arr)`

`# Creating a 2D array`
`arr_2d = np.array([[1, 2, 3], [4, 5, 6]])`
`print(arr_2d)`

`# Specifying data type`
`arr_float = np.array([1, 2, 3], dtype=float)`
`print(arr_float)`

## Key Points / Notes

- NumPy arrays are more efficient than Python lists for numerical operations.
- The `dtype` parameter allows you to specify the data type of the array elements.
- NumPy arrays support element-wise operations, making them suitable for mathematical computations.
