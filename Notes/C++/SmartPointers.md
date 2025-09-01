# Smart Pointers

## What is a Smart Pointer?

A **smart pointer** is an object that acts like a pointer but manages the lifetime of the object it points to. It automatically releases the allocated memory when it is no longer needed, helping to prevent **memory leaks** and **dangling pointers**.

Smart pointers are defined in the C++ Standard Library.

**Advantages over raw pointers:**
- Automatically delete the managed object when it goes out of scope
- Clearly express ownership semantics in code
- Reduce the need for manual `delete` calls
- Can be safely copied or moved depending on the type

## Types of Smart Pointers

- **std::unique_ptr** – Exclusive ownership, cannot be copied, only moved  
- **std::shared_ptr** – Shared ownership, reference-counted  
- **std::weak_ptr** – Non-owning reference to an object managed by `shared_ptr` (prevents cyclic references)

## Example: std::unique_ptr

#include <iostream>  
#include <memory>  

class MyClass {  
public:  
  MyClass() { std::cout << "Constructor\\n"; }  
  ~MyClass() { std::cout << "Destructor\\n"; }  
  void sayHello() { std::cout << "Hello from MyClass!\\n"; }  
};  

int main() {  
  std::unique_ptr<MyClass> ptr = std::make_unique<MyClass>();  
  ptr->sayHello();  
  // Destructor is called automatically when ptr goes out of scope  
  return 0;  
}  

**Output:**  
Constructor  
Hello from MyClass!  
Destructor  

## Example: std::shared_ptr and std::weak_ptr

#include <iostream>  
#include <memory>  

struct Node {  
    int value;  
    std::shared_ptr<Node> next;  
    std::weak_ptr<Node> prev; // prevents cyclic reference  
    Node(int val) : value(val) {}  
};  

int main() {  
    auto node1 = std::make_shared<Node>(1);  
    auto node2 = std::make_shared<Node>(2);  
    node1->next = node2;  
    node2->prev = node1; // weak_ptr avoids memory leak  

    std::cout << "Node1 value: " << node1->value << "\\n";  
    std::cout << "Node2 value: " << node2->value << "\\n";  
}  

## Key Points

- `std::unique_ptr` → sole ownership, lightweight, best for exclusive resources  
- `std::shared_ptr` → multiple owners, uses reference counting  
- `std::weak_ptr` → observes a shared_ptr without affecting its lifetime  
- Prefer `std::make_unique` / `std::make_shared` over `new` for **exception safety**

## Example Usage Summary

int main() {  
  auto uptr = std::make_unique<int>(42);   // unique_ptr  
  auto sptr = std::make_shared<int>(100);  // shared_ptr  
  std::weak_ptr<int> wptr = sptr;          // weak_ptr  
  std::cout << *uptr << " " << *sptr << "\\n"; // Output: 42 100  
}  
