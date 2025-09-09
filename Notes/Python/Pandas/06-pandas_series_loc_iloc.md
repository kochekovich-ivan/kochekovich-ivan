## loc — Label-based Indexing

- **Usage**: `series.loc[label]`
- **Accesses** elements by their **index label**.
- **Includes** both the start and stop labels in slicing.
- **Supports** boolean indexing and callable functions.

## iloc — Position-based Indexing

- **Usage**: `series.iloc[position]`
- **Accesses** elements by their **integer position**.
- **Excludes** the stop position in slicing.
- **Does not support** label-based indexing.

## Why It Matters

- **loc** is useful when you have meaningful index labels (e.g., dates, names).
- **iloc** is useful when you need to access elements based on their position in the Series.
- Both methods provide powerful tools for data selection and manipulation in pandas.
