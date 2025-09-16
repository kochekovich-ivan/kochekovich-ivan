## How `plot()` Works

- You import `matplotlib.pyplot` as `plt`.
- You pass data points (often as sequences like lists or arrays) to `plot()`.
- Key parameters allow control of how the line looks (color, marker, linestyle), labeling, etc.
- Finally, you display the plot with `plt.show()`.

## Examples

import matplotlib.pyplot as plt

# Basic line plot
``` Python
x = [0, 1, 2, 3, 4]
y = [0, 1, 4, 9, 16]
plt.plot(x, y)

plt.show()
```
# Plot with custom style
``` Python
x = [0, 1, 2, 3]
y = [10, 20, 15, 25]
plt.plot(x, y, color='red', linestyle='--', marker='o')

plt.title('Sample Plot')
plt.xlabel('X Axis')
plt.ylabel('Y Axis')
plt.grid(True)
plt.show()
```
# Multiple series in one plot
``` Python
x1 = [0, 1, 2, 3]
y1 = [1, 4, 9, 16]
x2 = [0, 1, 2, 3]
y2 = [1, 2, 3, 4]
plt.plot(x1, y1, label='Squares')
plt.plot(x2, y2, label='Linear')
plt.legend()
plt.show()
```
## Key Points / Notes

- The x- and y- data passed should align in length; mismatches cause errors.
- If you provide only one sequence, it’s assumed to be y; x defaults to the index range.
- Customization parameters include  
  • `color` — e.g. `'red'`, `'blue'`, `'#FF00FF'`  
  • `linestyle` — e.g. `'-'`, `'--'`, `':'`, `'-.`  
  • `marker` — e.g. `'o'`, `'s'`, `'^'`, `'*'`  
  • `label` — for legend entries  
- Use `plt.legend()` to display labels when multiple series are plotted.
- Effects like grid, axis labels, titles help readability.

## Applications / Use Cases

- Comparing multiple datasets in one figure.
- Visualizing trends, patterns, functions, or experimental data.
- Highlighting growth, decay, oscillations, etc.
- Creating publication-quality figures with customized styles.
