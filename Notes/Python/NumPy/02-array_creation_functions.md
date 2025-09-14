### 1. np.zeros()

Creates an array filled with zeros.

`import numpy as np`
`arr_zeros = np.zeros((3, 4))`

This creates a 3x4 array filled with zeros.

### 2. np.ones()

Creates an array filled with ones.

`arr_ones = np.ones((2, 5))`

This creates a 2x5 array filled with ones.

### 3. np.full()

Creates an array filled with a specified value.

`arr_full = np.full((2, 3), 7)`

This creates a 2x3 array filled with the value 7.

### 4. np.eye()

Creates a 2D identity matrix.

`arr_eye = np.eye(4)`

This creates a 4x4 identity matrix.

### 5. np.arange()

Creates an array with a range of values.

`arr_range = np.arange(0, 10, 2)`

This creates an array with values from 0 to 8, with a step size of 2.

### 6. np.linspace()

Creates an array with a specified number of evenly spaced values over a specified range.

`arr_linspace = np.linspace(0, 1, 5)`

This creates an array with 5 evenly spaced values from 0 to 1.

### 7. np.random.rand()

Creates an array with random values from a uniform distribution over [0, 1).

`arr_random = np.random.rand(2, 3)`

This creates a 2x3 array with random values.

### 8. np.random.randint()

Creates an array with random integers from a specified range.

`arr_randint = np.random.randint(1, 10, (2, 3))`

This creates a 2x3 array with random integers between 1 and 9.

### 9. np.random.randn()

Creates an array with random values from a standard normal distribution.

`arr_randn = np.random.randn(2, 3)`

This creates a 2x3 array with random values from a standard normal distribution.

## Key Points / Notes

- These functions are part of NumPy's array creation routines and are optimized for performance.
- They are useful for initializing arrays with specific patterns or values, which is common in numerical simulations and testing.
- The np.random functions provide ways to generate random numbers, which are essential for simulations and statistical modeling.
