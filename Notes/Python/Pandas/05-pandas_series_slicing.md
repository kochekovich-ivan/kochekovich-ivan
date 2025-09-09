## Slicing a Series

- **By position**: `s[start:stop]` — includes `start`, excludes `stop`.
- **By label**: `s['start_label':'end_label']` — includes both `start_label` and `end_label`.
- **Negative indexing**: `s[-n:]` — selects last `n` elements.
- **Step slicing**: `s[start:stop:step]` — selects elements with a step.

## Why It Matters

- Enables efficient data selection and manipulation.
- Useful for time series, filtering, and data analysis tasks.
