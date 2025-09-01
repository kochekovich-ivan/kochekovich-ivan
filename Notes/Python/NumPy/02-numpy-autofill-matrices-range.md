\# NumPy Array Creation and Initialization



In NumPy, there are multiple ways to create arrays. Let’s explore the most common ones.



\# Basic Initialization



If we want to create an array with 10 zeros, we can simply write:

`import numpy as np`



`a = np.array(\[0] \* 10)   # array of 10 zeros`

`b = np.array(\[1] \* 15)   # array of 15 ones`



But NumPy provides faster and more convenient methods:



`np.zeros(shape, dtype=float)` → returns an array filled with zeros.



`np.ones(shape, dtype=float)` → returns an array filled with ones.



`np.full(shape, value, dtype=None)` → returns an array filled with a specific value.



`np.empty(shape, dtype=float)` → returns an uninitialized array (values are random).



Example:

`zeros\_arr = np.zeros(10)`             # \[0. 0. 0. ...]

`ones\_arr = np.ones((3, 3), int)`      # 3x3 matrix of ones

`full\_arr = np.full((2, 5), 7)`        # 2x5 matrix filled with 7



\# Identity and Diagonal Matrices



np.eye(N, M=None) → creates an identity-like matrix with ones on the main diagonal.



np.identity(n) → square identity matrix of size n.



np.diag(v, k=0) → creates a diagonal matrix from vector v.



np.diagflat(v) → places a 1D array on the diagonal of a 2D array.



Example:

`I = np.eye(4)        # 4x4 identity matrix`

`D = np.diag(\[1, 2, 3])`



\# Range Functions



NumPy also has powerful tools for generating numeric ranges:



np.arange(start, stop, step) → similar to Python’s range, but returns an array.



np.linspace(start, stop, num) → returns evenly spaced values between start and stop.



np.logspace(start, stop, num) → values spaced on a log scale.



np.geomspace(start, stop, num) → values spaced on a geometric scale.



Example:

`a = np.arange(0, 10, 2)       # \[0 2 4 6 8]`

`b = np.linspace(0, 1, 5)      # \[0. 0.25 0.5 0.75 1.]`

`c = np.logspace(1, 3, 3)      # \[10. 100. 1000.]`



\# Grid Generation



For creating coordinate matrices:



np.mgrid\[] → returns dense multi-dimensional grids.



np.ogrid\[] → returns open grids (memory-efficient).



Example:

x, y = np.mgrid\[0:3, 0:3]





\# Other Array Constructors



np.array(object) → creates array from Python sequence.



np.asanyarray(a), np.asarray(a) → convert input to array.



np.copy(a) → returns a copy of array.



np.fromfunction(function, shape) → construct array from a function.



np.fromiter(iterable, dtype) → create array from iterable.



np.loadtxt(file), np.fromfile() → load data from file.





