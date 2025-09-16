## Examples
``` Python
import numpy as np  
import matplotlib.pyplot as plt  

# Using subplot()
plt.subplot(1, 3, 1)  
plt.plot(np.random.random(10))  

plt.subplot(1, 3, 2)  
plt.plot(np.random.random(10))  

plt.subplot(1, 3, 3)  
plt.plot(np.random.random(10))  

plt.grid()  
plt.show()
```
# Using variable references and setting grid for each axis
``` Python
ax1 = plt.subplot(1, 3, 1)  
plt.plot(np.random.random(10))  
ax2 = plt.subplot(1, 3, 2)  
plt.plot(np.random.random(10))  
ax3 = plt.subplot(1, 3, 3)  
plt.plot(np.random.random(10))  

ax1.grid()  
ax2.grid()  
ax3.grid()  
plt.show()
```
# Using subplots()
``` Python
f, ax = plt.subplots(2, 2)  
ax[0, 0].plot(np.arange(0, 5, 0.2))  
ax[0, 0].grid()  
ax[0, 1].plot(np.arange(5, 0, -0.2))  
ax[0, 1].grid()  
plt.show()
```
# Using arbitrary axes positioning
``` Python
fig = plt.figure(figsize=(7, 4))  
ax1 = fig.add_axes([0.0, 0, 1.0, 1.0])  
ax1.plot(np.arange(0, 5, 0.2))  
plt.show()
```
# Using GridSpec
``` Python
from matplotlib.gridspec import GridSpec  
fig = plt.figure(figsize=(7, 4))  
gs = GridSpec(ncols=3, nrows=2, figure=fig)  

ax1 = plt.subplot(gs[0, 0])  
ax1.plot(np.arange(0, 5, 0.2))  
ax2 = fig.add_subplot(gs[1, 0:2])  
ax2.plot(np.random.random(10))  
ax3 = fig.add_subplot(gs[:, 2])  
ax3.plot(np.random.random(10))  

plt.show()
```
## Key Points / Notes

- `subplot(nrows, ncols, index)` divides the figure into a grid of `nrows × ncols` and selects the subplot at position `index`.  
- The integer version `subplot(abc)` where `a`, `b`, `c` are digits (if `nrows < 10` and `ncols < 10`) is shorthand for `subplot(a, b, c)`.  
- `subplots(nrows, ncols)` returns a tuple `(Figure, Axes_array)`, which is more convenient when working with many axes.  
- You can share axes (e.g. `sharex`, `sharey`) in `subplots()` to align scales or reduce label clutter.  
- `add_axes([left, bottom, width, height])` allows placing axes at an arbitrary position and size within the figure; values are fractions between 0 and 1.  
- `GridSpec` provides flexible control over subplot layout, allowing axes to span multiple rows or columns.  
- Use `fig.set_size_inches(...)` or `figsize=...` in `figure()` or `subplots()` to control the overall figure size.  
- Use `ax.grid()` to enable grid on a specific axis. Calling `plt.grid()` only affects the currently active axis.

## Applications / Use Cases

- Comparing multiple related plots side by side (e.g. different variables, different timeframes).  
- Displaying summary and detail plots in one figure.  
- Creating complex dashboards of charts with shared scales.  
- Custom layouts for publication or presentation-ready figures.  
- Emphasizing part of data via inset axes or zoomed subplots.
