## Explanation

A **Singly Linked List** is a type of linked list where each node contains:
- **Data**: the value stored in the node.
- **Next pointer**: points to the next node in the list.

Traversal is **forward only**, from the head to the last node. The last node’s `next` pointer is `nullptr`.

## Structure of a Node
``` C++
Node {  
    int data;  
    Node* next;
    Node(int val) : data(val), next(nullptr) {}
}
```
- **Head**: pointer to the first node of the list.
- **Tail**: last node whose `next` is `nullptr`.

## Key Operations

### 1. Insertion
- **At beginning**: new node points to current head, then head is updated.  
- **At end**: traverse to last node and attach new node.  
- **At position**: traverse to position, update pointers to insert new node.

### 2. Deletion
- **At beginning**: move head to next node and delete old head.  
- **At end**: traverse to second-last node, set `next` to `nullptr`, delete last node.  
- **At position**: update previous node’s `next` pointer to skip target node, then delete it.

### 3. Traversal
- Start from head and follow `next` pointers until `nullptr`.  

### 4. Search
- Iterate through each node comparing `data` until a match is found.

## Advantages

- Dynamic memory allocation (can grow/shrink at runtime).  
- Efficient insertions/deletions at the beginning.  
- No need to predefine size (unlike arrays).

## Disadvantages

- Only forward traversal.  
- No random access (must traverse sequentially).  
- Extra memory for `next` pointers.  

## Applications / Use Cases

- Implementing stacks and queues.  
- Representing sequences with frequent insertions/deletions.  
- Dynamic memory management in operating systems.  
- Simple list-based data storage when backward traversal is not needed.

## Key Points / Notes

- Always handle memory properly using `new` and `delete` to avoid leaks.  
- Keep track of the head pointer for all operations.  
- Avoid accessing `next` of `nullptr` to prevent segmentation faults.  
