### Changing Array Shape

The reshape() method allows you to change the shape of an existing array without changing its data.

``import numpy as np
arr = np.array([1, 2, 3, 4, 5, 6])
reshaped_arr = arr.reshape(2, 3)``

This reshapes the 1D array into a 2D array with 2 rows and 3 columns.

### Adding Axes

To add an axis (i.e., increase the number of dimensions), you can use np.newaxis or reshape().

``arr = np.array([1, 2, 3])
arr_2d = arr[:, np.newaxis]``

This converts the 1D array into a 2D column vector.

Alternatively, using reshape():

`arr_2d = arr.reshape(-1, 1)`

This also converts the 1D array into a 2D column vector.

### Removing Axes

To remove an axis (i.e., reduce the number of dimensions), you can use np.squeeze().

``arr = np.array([[[1], [2], [3]]])
squeezed_arr = np.squeeze(arr)``

This removes the singleton dimensions, resulting in a 1D array.

### Transposing Arrays

Transposing swaps the rows and columns of a 2D array.

``arr = np.array([[1, 2, 3], [4, 5, 6]])
transposed_arr = arr.T``

This swaps the rows and columns of the 2D array.

## Key Points / Notes

- reshape() does not modify the original array; it returns a new array with the specified shape.
- Using np.newaxis or reshape() with -1 allows for flexible dimension manipulation.
- np.squeeze() removes all singleton dimensions, which is useful for eliminating unnecessary axes.
- Transposing is commonly used in linear algebra and data manipulation tasks.
