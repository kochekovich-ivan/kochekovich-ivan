# Queue

## Definition
- **Queue** is a linear data structure that follows **FIFO** (First In, First Out) principle.
- The first element added is the first one removed.

## Main Operations
- **enqueue(x)** — add element x to the rear (end) of the queue.
- **dequeue()** — remove and return the front element.
- **front() / peek()** — return the front element without removing it.
- **isEmpty()** — check if the queue has no elements.
- **size()** — return number of elements.

## Example
Initial queue: [ ]  
enqueue(10) → [10]  
enqueue(20) → [10, 20]  
dequeue() → returns 10, queue becomes [20]

## Use Cases
- Task scheduling (printer queue, OS process scheduling)
- Breadth-First Search (BFS) in graphs
- Handling requests in real-time systems
- Buffers in data streams (e.g., keyboard input)

## Implementation
- Can be implemented using:
  - Array (circular buffer recommended to avoid shifting)
  - Linked list (dynamic size)
  - Built-in classes:  
    - C++ → std::queue  
    - Python → collections.deque or queue.Queue  

## Complexity
- Enqueue, Dequeue, Peek: **O(1)**
- Memory: proportional to number of elements (O(n))
