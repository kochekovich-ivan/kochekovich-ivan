# BST

## Structure

- Each node contains:
  - `key`
  - pointer to `left` child
  - pointer to `right` child

## Key Operations

### Insertion
- Start from the root.
- If the new value is smaller, go left; if larger, go right.
- Insert at the correct null position.

### Search
- Compare value with current node.
- If equal → found.
- If smaller → go left, if larger → go right.
- Stop when node is null (not found).

### Deletion
Three cases:
1. **Leaf node** → simply delete.
2. **One child** → replace node with its child.
3. **Two children** → replace with inorder successor (smallest in right subtree) or inorder predecessor (largest in left subtree).

### Traversals
- **Inorder (LNR):** left → node → right → gives sorted order.
- **Preorder (NLR):** node → left → right.
- **Postorder (LRN):** left → right → node.

## Time Complexity

- Average case: O(log n) for search, insert, delete.
- Worst case (unbalanced tree): O(n).

## Key Points / Notes

- BST efficiency depends on balance of the tree.
- For guaranteed performance, use **balanced BSTs** (AVL, Red-Black).
- Recursive implementations are simpler, iterative can save memory.
- Must handle duplicates explicitly (ignore, count, or store consistently).

## Applications / Use Cases

- Efficient searching and sorting.
- Implementing associative containers (map, set).
- Maintaining ordered data dynamically.
- Used as the foundation for balanced tree structures in STL.
