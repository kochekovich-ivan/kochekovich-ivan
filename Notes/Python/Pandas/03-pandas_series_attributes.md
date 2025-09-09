## Key Attributes of Series
- **index**: labels for each element (default numeric, can be custom).
- **values**: underlying data as NumPy array or array-like.
- **dtype**: data type of the series elements.
- **shape** / **size**: dimensions (always 1D) and count of elements.
- **name**: optional name for the Series.
- **empty**: indicates whether Series has no data.
- **hasnans**: checks if the Series contains missing values.
- **is_unique**: checks if all values are distinct.
- **is_monotonic_increasing / _decreasing**: checks if data is sorted.
- **memory_usage** and **nbytes**: show memory consumed by Series.

## Why These Attributes Are Useful
- Provide essential metadata about the Series (size, type, memory).
- Help understand structure and behavior without manual inspection.
- Useful in data validation and exploratory analysis.
