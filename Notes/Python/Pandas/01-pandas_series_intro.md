## What Is a Series?
- A one-dimensional labeled array in pandas.
- Similar to a DataFrame column or spreadsheet column.
- Can store any type of data: numbers, strings, booleans, objects.

## Indexing Basics
- Default index is numeric (0, 1, 2, …).
- You can set custom labels for index.
- Elements can be accessed by:
  - Position (e.g., s[0])
  - Label (e.g., s["label"])

## Creating a Series
- From a list: `pd.Series([1, 2, 3])`
- From a dictionary: keys become index labels.
- From a scalar with explicit index: value is repeated for each label.

## Why It Matters
- Fundamental building block in pandas.
- Every DataFrame column is a Series.
- Combines NumPy’s efficiency with flexible labeling and indexing.
