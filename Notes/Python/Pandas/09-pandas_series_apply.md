## Purpose
- Applies a function to each element in a Series.

## Key Parameters
- func — function to apply to each element
- convert_dtype — True (default) tries to find a better dtype for the result
- args — positional arguments passed to func after the series value
- kwds — additional keyword arguments passed to func

## Examples

# Creating a Series
s = pd.Series([10, 20, 30])

# Applying a function to square each element
s.apply(lambda x: x**2)

# Applying a function with additional arguments
def subtract_custom_value(x, custom_value):
    return x - custom_value

s.apply(subtract_custom_value, args=(5,))

## Why It Matters
- Enables element-wise transformations and computations.
- Useful for data preprocessing and feature engineering.
- Allows for custom operations not covered by built-in methods.
