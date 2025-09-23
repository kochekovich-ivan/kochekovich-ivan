## Explanation

A **Doubly Linked List (DLL)** is a linked list where each node contains:
- **Data**: the value stored in the node.
- **Next pointer**: points to the next node.
- **Previous pointer**: points to the previous node.

Traversal can be **both forward and backward**, unlike a singly linked list.

## Structure of a Node
``` C++
Node {  
    int data;  
    Node* next;  
    Node* prev;
    Node(int val) : data(val), next(nullptr), prev(nullptr) {} 
}
```
- **Head**: pointer to the first node.  
- **Tail**: pointer to the last node (`next` is `nullptr`).

## Key Operations

### 1. Insertion
- **At beginning**: new node points `next` to current head, `prev` to nullptr, update head’s `prev`, then update head.  
- **At end**: traverse to tail, set tail’s `next` to new node, new node’s `prev` to tail, update tail.  
- **At position**: traverse to desired position, adjust `next` and `prev` pointers of neighboring nodes to insert new node.

### 2. Deletion
- **At beginning**: move head to next node, set head’s `prev` to nullptr, delete old head.  
- **At end**: move tail to previous node, set tail’s `next` to nullptr, delete old tail.  
- **At position**: update `next` of previous node and `prev` of next node to skip target node, then delete it.

### 3. Traversal
- **Forward**: from head, follow `next` pointers until `nullptr`.  
- **Backward**: from tail, follow `prev` pointers until `nullptr`.

### 4. Search
- Iterate through nodes using `next` or `prev` pointers to find the target data.

## Advantages

- Supports bidirectional traversal.  
- Easier insertion and deletion at both ends.  
- More flexible than singly linked lists for certain operations.

## Disadvantages

- Extra memory needed for `prev` pointers.  
- Slightly more complex operations due to pointer adjustments.  
- Risk of dangling pointers if not handled correctly.

## Applications / Use Cases

- Implementing dequeues (double-ended queues).  
- Undo/redo functionality in software (forward/backward movement).  
- Navigation systems with previous/next references.  
- Complex data structures like adjacency lists for graphs.  

## Key Points / Notes

- Carefully manage `next` and `prev` pointers during insertion/deletion.  
- Head and tail pointers must always be updated when modifying the ends.  
- Memory management is crucial: always delete nodes to avoid leaks.  
