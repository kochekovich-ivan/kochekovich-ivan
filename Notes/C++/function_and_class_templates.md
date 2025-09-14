# Templates (Function and Class)

## What Templates Are
- **Templates** are a way to write code once and use it with many different data types.
- The compiler generates the actual version of the function or class for each type used.
- Main idea: write generic code that adapts to the type automatically.

## Function Templates
- Let you create functions that work with any data type.
- The type is chosen automatically when you call the function.
- Example in words: "one universal `add` function" that works with ints, doubles, strings — no need to write separate versions.

## Class Templates
- Let you create classes that store or work with different types without rewriting the class.
- Example in words: "one universal container class" that can hold integers, strings, or any other type.

## Why Templates Are Important
- Reduce code duplication.
- Increase code flexibility and reusability.
- Used everywhere in the C++ Standard Template Library (STL): vectors, queues, maps.

## Key Points
- `typename` and `class` mean the same thing in template definitions.
- Compiler creates a separate version of the function/class for each type you use.
- Templates are resolved at compile time → efficient but can slow compilation and give long error messages.
