## Explanation

A **Queue** is a linear data structure that follows the **FIFO (First In, First Out)** principle: the first element inserted is the first one to be removed.  
It is commonly used in scenarios where order of processing matters.

## Structure

- **Front**: points to the first element of the queue.  
- **Rear**: points to the last element inserted.  
- Can be implemented using:
  - **Array** (static or circular array)  
  - **Linked List** (dynamic size)  

## Key Operations

### 1. Enqueue
- Add an element to the rear of the queue.  
- Check for overflow if array-based.

### 2. Dequeue
- Remove an element from the front of the queue.  
- Check for underflow if queue is empty.

### 3. Peek / Front
- Access the front element without removing it.

### 4. IsEmpty / IsFull
- Check whether the queue is empty or full (for arrays).

## Example (Conceptual)
``` C++
Queue = []  
Enqueue(10) → [10]  
Enqueue(20) → [10, 20]  
Dequeue() → returns 10, Queue = [20]  
Peek() → returns 20  
```
## Types of Queues

1. **Simple Queue**  
   - Linear queue with front and rear pointers.  

2. **Circular Queue**  
   - Rear wraps around to the beginning when reaching end of array.  
   - Efficient memory usage.  

3. **Priority Queue**  
   - Each element has a priority; higher priority elements are dequeued first.  

4. **Deque (Double-Ended Queue)**  
   - Insertion and deletion can occur at both front and rear.

## Advantages

- Maintains processing order.  
- Simple and efficient for sequential access.  
- Supports O(1) enqueue and dequeue in linked list implementation.

## Disadvantages

- Access is limited to front and rear only.  
- Array-based queues can require shifting elements (unless circular).  

## Applications / Use Cases

- CPU task scheduling (ready queue).  
- Print spooling in operating systems.  
- Handling requests in web servers.  
- BFS (Breadth-First Search) in graphs.  
- Call center and ticketing systems.

## Key Points / Notes

- Queue follows **FIFO** principle.  
- Circular queues avoid wasted space in array implementation.  
- Linked list queues allow dynamic size and avoid overflow.  
