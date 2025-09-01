\# What is a Smart Pointer?



A smart pointer is an object that acts like a pointer but manages the lifetime of the object it points to. It automatically releases the allocated memory when it is no longer needed, helping to prevent memory leaks and dangling pointers.



Smart pointers are defined in the <memory> header and are part of the C++ Standard Library.



Unlike raw pointers, smart pointers:



&nbsp;   Automatically delete the managed object when it goes out of scope.



&nbsp;   Clearly express ownership semantics in code.



&nbsp;   Reduce the need for manual delete calls.



&nbsp;   Can be safely copied or moved depending on the type.



\# Types of Smart Pointers



&nbsp;   std::unique\_ptr – Exclusive ownership, cannot be copied, only moved.



&nbsp;   std::shared\_ptr – Shared ownership, reference-counted.



&nbsp;   std::weak\_ptr – Non-owning reference to an object managed by std::shared\_ptr.



Example: std::unique\_ptr



`#include <iostream>`

`#include <memory>`



`class MyClass {`

`public:`

&nbsp;   `MyClass() { std::cout << "Constructor\\n"; }`

&nbsp;   `~MyClass() { std::cout << "Destructor\\n"; }`

&nbsp;   `void sayHello() { std::cout << "Hello from MyClass!\\n"; }`

`};`



`int main() {`

&nbsp;   `std::unique\_ptr<MyClass> ptr = std::make\_unique<MyClass>();`

&nbsp;   `ptr->sayHello();`



&nbsp;   // No need to manually delete — destructor is called automatically

&nbsp;   `return 0;`

`}`



Output:



Constructor

Hello from MyClass!

Destructor





\# Example: std::shared\_ptr and std::weak\_ptr

`#include <iostream>`

`#include <memory>`



`struct Node {`

`    int value;`

`    std::shared\_ptr<Node> next;`

`    std::weak\_ptr<Node> prev; // prevents cyclic reference`



`    Node(int val) : value(val) {}`

`};`



`int main() {`

&nbsp;`   auto node1 = std::make\_shared<Node>(1);`

&nbsp; `  auto node2 = std::make\_shared<Node>(2);`



`    node1->next = node2;`

&nbsp;`   node2->prev = node1; // weak\_ptr avoids memory leak`



`    std::cout << "Node1 value: " << node1->value << "\\n";`

&nbsp;`   std::cout << "Node2 value: " << node2->value << "\\n";`

`}`



\# Key Points



&nbsp;   std::unique\_ptr → sole ownership, lightweight, best for exclusive resources.



&nbsp;   std::shared\_ptr → multiple owners, uses reference counting.



&nbsp;   std::weak\_ptr → observes a shared\_ptr without affecting its lifetime.



&nbsp;   Prefer std::make\_unique / std::make\_shared over new for exception safety.



\# Example Usage Summary



`int main() {`

&nbsp;   `auto uptr = std::make\_unique<int>(42);   // unique\_ptr`

&nbsp;   `auto sptr = std::make\_shared<int>(100);  // shared\_ptr`

&nbsp;   `std::weak\_ptr<int> wptr = sptr;          // weak\_ptr`



&nbsp;   `std::cout << \*uptr << " " << \*sptr << "\\n"; // Output: 42 100`

`}`





