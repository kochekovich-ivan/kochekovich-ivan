## 1. Creating Arrays in NumPy

To create an array in NumPy, use the array() function.

Example:
import numpy as np
a = np.array([1, 2, 3, 4, 5])
print(a)

You can specify the data type:
a = np.array([1, 2, 3, 4, 5], dtype=np.int32)
print(a.dtype)  # int32

### Common Data Types

- bool_ – Boolean type (1 byte)  
- int_ – Default integer (4 or 8 bytes, depends on system)  
- int8, int16, int32, int64 – Signed integers (1,2,4,8 bytes)  
- uint8, uint16, uint32, uint64 – Unsigned integers  
- float_ – Floating point (default 8 bytes = float64)  
- float16, float32, float64 – Floating-point numbers with different precision  
- str_ – String type  

### Type Conversion

x = np.float64(10)  # converts 10 to 10.0

arr = np.array([1.7, 2.3, 3.9])
arr_int = arr.astype(np.int32)  # [1 2 3]

Be careful: converting float to int truncates the fractional part. Overflow may occur if the value is out of range.

---

## 2. Array Creation and Initialization

### Using convenience functions

zeros_arr = np.zeros(10)           # 1D array of zeros
ones_arr = np.ones((3,3), int)     # 3x3 array of ones
full_arr = np.full((2,5), 7)       # 2x5 array filled with 7

- np.zeros(shape, dtype=float) → array of zeros  
- np.ones(shape, dtype=float) → array of ones  
- np.full(shape, value, dtype=None) → array filled with value  
- np.empty(shape, dtype=float) → uninitialized array  

### Identity and Diagonal Matrices

- np.eye(N, M=None) → identity-like matrix with ones on the main diagonal  
- np.identity(n) → square identity matrix  
- np.diag(v, k=0) → diagonal matrix from vector v  
- np.diagflat(v) → place 1D array on the diagonal of 2D array  

Example:
I = np.eye(4)
D = np.diag([1,2,3])

---

## 3. Numeric Ranges

- np.arange(start, stop, step) → array of numbers  
- np.linspace(start, stop, num) → evenly spaced numbers  
- np.logspace(start, stop, num) → log-spaced numbers  
- np.geomspace(start, stop, num) → geometric spaced numbers  

Example:
a = np.arange(0,10,2)   # [0 2 4 6 8]
b = np.linspace(0,1,5)  # [0. 0.25 0.5 0.75 1.]
c = np.logspace(1,3,3)  # [10. 100. 1000.]

---

## 4. Grid Generation

- np.mgrid[] → dense multi-dimensional grids  
- np.ogrid[] → open grids (memory-efficient)  

Example:
x, y = np.mgrid[0:3, 0:3]

---

## 5. Other Array Constructors

- np.array(object) → create array from Python sequence  
- np.asanyarray(a), np.asarray(a) → convert input to array  
- np.copy(a) → copy of an array  
- np.fromfunction(function, shape) → array from function  
- np.fromiter(iterable, dtype) → array from iterable  
- np.loadtxt(file), np.fromfile() → load data from file
