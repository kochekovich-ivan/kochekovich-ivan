## Explanation

A **Stack** is a linear data structure that follows the **LIFO (Last In, First Out)** principle: the last element inserted is the first one to be removed.  
Stacks are used in situations where reverse-order processing is needed.

## Structure

- **Top**: pointer or index to the last inserted element.  
- Stack elements can be stored in:
  - **Array** (fixed size)  
  - **Linked List** (dynamic size)  

## Key Operations

### 1. Push
- Add an element to the top of the stack.  
- If array-based, check for overflow (stack full).  

### 2. Pop
- Remove the top element from the stack.  
- If stack is empty, handle underflow.

### 3. Peek / Top
- Access the top element without removing it.  

### 4. IsEmpty / IsFull
- Check whether the stack is empty or full (for arrays).  

## Example (Conceptual)

Stack = []  
Push(10) → [10]  
Push(20) → [10, 20]  
Pop() → returns 20, Stack = [10]  
Peek() → returns 10  

## Advantages

- Simple and easy to implement.  
- Efficient O(1) time for push and pop.  
- Supports recursion, undo mechanisms, expression evaluation.

## Disadvantages

- Limited access: can only access the top element.  
- Array-based stacks have fixed size unless dynamically resized.

## Applications / Use Cases

- Function call management (call stack) in programming languages.  
- Undo/redo operations in software.  
- Expression evaluation and syntax parsing (infix, postfix, prefix).  
- Backtracking algorithms (e.g., maze solving, pathfinding).  
- Browser history navigation (back/forward).

## Key Points / Notes

- Stack can be implemented using **arrays** or **linked lists**.  
- Always handle underflow and overflow conditions.  
- LIFO principle is the defining feature of stack operations.  
