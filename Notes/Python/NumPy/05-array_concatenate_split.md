### Concatenating Arrays

Concatenation is the process of joining two or more arrays along an existing axis.

- np.concatenate(): Joins a sequence of arrays along an existing axis.

``import numpy as np
arr1 = np.array([[1, 2], [3, 4]])
arr2 = np.array([[5, 6]])
concatenated_arr = np.concatenate((arr1, arr2), axis=0)``

This joins arr1 and arr2 along the first axis (rows), resulting in a 3x2 array.

- np.vstack(): Stacks arrays in sequence vertically (row-wise).

`stacked_arr = np.vstack((arr1, arr2))`

This stacks arr1 and arr2 vertically, resulting in a 3x2 array.

- np.hstack(): Stacks arrays in sequence horizontally (column-wise).

``arr3 = np.array([[7], [8]])
stacked_arr = np.hstack((arr1, arr3))``

This stacks arr1 and arr3 horizontally, resulting in a 2x3 array.

### Splitting Arrays

Splitting is the process of dividing an array into multiple sub-arrays.

- np.split(): Splits an array into multiple sub-arrays.

``arr = np.array([1, 2, 3, 4, 5, 6])
split_arr = np.split(arr, 3)``

This splits arr into 3 sub-arrays: [1, 2], [3, 4], and [5, 6].

- np.hsplit(): Splits an array into multiple sub-arrays horizontally (column-wise).

``arr = np.array([[1, 2, 3], [4, 5, 6]])
split_arr = np.hsplit(arr, 3)``

This splits arr into 3 sub-arrays along the columns.

- np.vsplit(): Splits an array into multiple sub-arrays vertically (row-wise).

``arr = np.array([[1, 2], [3, 4], [5, 6]])
split_arr = np.vsplit(arr, 3)``

This splits arr into 3 sub-arrays along the rows.

## Key Points / Notes

- Ensure that the dimensions of the arrays are compatible when concatenating along a specific axis.
- Splitting an array requires specifying the number of splits or the indices at which to split.
- These operations return new arrays and do not modify the original arrays.
