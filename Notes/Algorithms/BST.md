## Explanation

A **Binary Search Tree (BST)** is a hierarchical data structure where each node has:
- **Key/Value**  
- **Left child** (all keys smaller than node)  
- **Right child** (all keys larger than node)  

BST allows efficient searching, insertion, and deletion by leveraging this ordering property.

## Key Operations

### 1. Insertion
- Start at the root.  
- Compare value with current node:  
  - If smaller → go left  
  - If larger → go right  
- Insert at null position when reached.

### 2. Search
- Compare target with node key:  
  - Equal → found  
  - Smaller → search left subtree  
  - Larger → search right subtree  

### 3. Deletion
Three cases:
1. **Leaf node** → delete directly.  
2. **Node with one child** → replace node with its child.  
3. **Node with two children** → replace with inorder successor (smallest in right subtree) or predecessor.

### 4. Traversals
- **Inorder (LNR)** → sorted order  
- **Preorder (NLR)** → root first  
- **Postorder (LRN)** → root last  

## Advantages

- Efficient search, insertion, and deletion (average O(log n)).  
- Ordered structure allows easy retrieval of sorted data.

## Disadvantages

- Performance depends on tree balance.  
- Worst case (skewed tree) → O(n) operations.  

## Applications / Use Cases

- Implementing associative containers (maps, sets).  
- Dynamic sorted data storage.  
- Basis for balanced trees (AVL, Red-Black Trees).  
- Search optimization in databases.

## Key Points / Notes

- Avoid skewed trees; balance improves performance.  
- Recursive or iterative implementations possible.  
- Can handle duplicates based on chosen policy (ignore, count, or store consistently).  
