## Examples
``` Python
import matplotlib.pyplot as plt  
import numpy as np  
import matplotlib.ticker as ticker  
```
# Example: set axis limits and custom locators
``` Python
x = np.linspace(0, 10, 100)  
y = np.sin(x)  

fig, ax = plt.subplots(figsize=(6,4))  
ax.plot(x, y)  
```
# Set axis limits
``` Python
ax.set_xlim(0, 10)  
ax.set_ylim(-1.5, 1.5)  
```
# Major ticks every π
``` Python
major_locator = ticker.MultipleLocator(np.pi)  
ax.xaxis.set_major_locator(major_locator)  
```
# Minor ticks every π/4
``` Python
minor_locator = ticker.MultipleLocator(np.pi / 4)  
ax.xaxis.set_minor_locator(minor_locator)  
```
# Format major tick labels with multiples of π
``` Python
major_formatter = ticker.FuncFormatter(lambda val, pos:  
    f"{val/np.pi:.0f}π" if val != 0 else "0")  
ax.xaxis.set_major_formatter(major_formatter)  
```
# Optional: style ticks
``` Python
ax.tick_params(which='major', length=7, width=1.5)  
ax.tick_params(which='minor', length=4, width=1)  

plt.show()
```
## Key Points / Notes

- `.set_xlim(left, right)` and `.set_ylim(bottom, top)` control the visible range of the x‐ and y‐axes.  
- Locators decide *where* ticks are placed. Formatters decide *how* tick labels are shown.  
- Common Locator types:
  - `MultipleLocator(base)` – ticks at multiples of a base value.  
  - `FixedLocator([...])` – ticks at fixed positions.  
  - `AutoLocator()` / `MaxNLocator(n)` – automatic spacing, up to `n` ticks.  
  - `LogLocator` – for log‐scaled axes.  
- Minor ticks: useful for finer granularity but usually without labels.  
- Use `ax.tick_params()` to adjust tick appearance: size, width, direction, which (major/minor), etc.  

## Applications / Use Cases

- Making plots where axes need to start/end at specific values (like 0 or round numbers).  
- Ensuring multiple subplots share the same axis limits for comparison.  
- Showing data on log scales.  
- Using clean, meaningful tick labels (e.g. multiples of π, dates, etc.).  
- Improving readability in plots with dense or many ticks.  
