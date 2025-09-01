\# How to Create an Array in NumPy



To create an array in NumPy, you use the array() function.

Example:

`import numpy as np`



`a = np.array(\\\[1, 2, 3, 4, 5])`

`print(a)`

Now a is an array with 5 elements. Unlike C++, you can just print() the array directly.



If you want to specify the data type, use the dtype parameter:

`a = np.array(\\\[1, 2, 3, 4, 5], dtype=np.int32)`

`print(a.dtype)   # int32`



\# Common Data Types in NumPy



bool\_ – Boolean type (1 byte)



int\_ – Default integer (4 or 8 bytes, depends on system)



int8, int16, int32, int64 – Signed integers (1, 2, 4, 8 bytes)



uint8, uint16, uint32, uint64 – Unsigned integers (cannot be negative)



float\_ – Floating point (default 8 bytes = float64)



float16, float32, float64 – Floating-point numbers with different precision



str\_ – String type



\# Type Conversion



You can cast values to another type:

`x = np.float64(10)   # result: 10.0`



You can also convert the entire array:

`arr = np.array(\\\[1.7, 2.3, 3.9])`

`arr\\\_int = arr.astype(np.int32)   # \\\[1 2 3]`





\# Be careful:



When converting from float → int, the fractional part is truncated.



Overflow can happen if the number is outside the type’s range:



`a = np.array(\\\[1, 2, 1000, 256], dtype=np.int8)`

`print(a)   # \\\[  1   2 -24   0]`



\# Multidimensional Arrays



NumPy can also create matrices (2D arrays):

`a = np.array(\[\[1, 2],`
	      `\[3, 4],`
	      `\[5, 6]])`
`print(a)`

