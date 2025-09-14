# Function and Class Templates

## Purpose
- **Templates** allow writing generic code that works with any data type.
- Avoid code duplication for functions/classes that differ only by type.

## Function Template

Syntax:

`template <typename T>`
`T add(T a, T b)`
`{`
    `return a + b;`
`}`

Usage:
- add(3, 5) → works with int
- add(3.5, 2.1) → works with double

## Class Template

Syntax:

`template <typename T>`
`class Box`
`{`
`private:`
`    T value;`
`public:`
`    Box(T v) : value(v) {}`
`    T get() { return value; }`
`};`

Usage:

Box<int> b1(10);
Box<std::string> b2("Hello");

## Key Notes
- `typename` and `class` keywords are interchangeable in template parameter list.
- Template functions are instantiated by compiler with required types at compile time.
- Can specify multiple type parameters:

`template <typename T1, typename T2>`
`auto multiply(T1 a, T2 b) { return a * b; }`

## Benefits
- Code reuse for multiple types.
- Type safety (compile-time checking).
- Foundation for STL (Standard Template Library).

## Limitations
- Template code increases compile time.
- Compiler generates separate instantiations for each type → bigger binary.
- Error messages can be complex.
