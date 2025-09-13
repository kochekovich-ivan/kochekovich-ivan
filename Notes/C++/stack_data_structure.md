# Stack

## Definition
- **Stack** is a linear data structure that follows **LIFO** (Last In, First Out) principle.
- The last element added is the first one removed.

## Main Operations
- **push(x)** — add element x to the top of the stack.
- **pop()** — remove and return the top element.
- **peek() / top()** — return the top element without removing it.
- **isEmpty()** — check if stack has no elements.
- **size()** — return number of elements.

## Example
Initial stack: [ ]  
push(10) → [10]  
push(20) → [10, 20]  
pop() → returns 20, stack becomes [10]

## Use Cases
- Function call management (call stack)
- Undo/Redo operations in editors
- Parsing (balanced parentheses, expressions)
- Backtracking algorithms (DFS)

## Implementation
- Can be implemented using:
  - Array (fixed size, O(1) access)
  - Linked list (dynamic size)
  - Built-in classes:  
    - C++ → std::stack  
    - Python → list or collections.deque  

## Complexity
- Push, Pop, Peek: **O(1)**
- Memory: proportional to number of elements (O(n))
