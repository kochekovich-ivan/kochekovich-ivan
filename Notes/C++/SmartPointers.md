\# What is a Smart Pointer?



A smart pointer is an object that acts like a pointer but manages the lifetime of the object it points to. It automatically releases the allocated memory when it is no longer needed, helping to prevent memory leaks and dangling pointers.



Smart pointers are defined in the <memory> header and are part of the C++ Standard Library.



Unlike raw pointers, smart pointers:



    Automatically delete the managed object when it goes out of scope.



    Clearly express ownership semantics in code.



    Reduce the need for manual delete calls.



    Can be safely copied or moved depending on the type.



\# Types of Smart Pointers



    std::unique\_ptr – Exclusive ownership, cannot be copied, only moved.



    std::shared\_ptr – Shared ownership, reference-counted.



    std::weak\_ptr – Non-owning reference to an object managed by std::shared\_ptr.



Example: std::unique\_ptr



`#include <iostream>`

`#include <memory>`



`class MyClass {`

`public:`

    `MyClass() { std::cout << "Constructor\\\\n"; }`

    `~MyClass() { std::cout << "Destructor\\\\n"; }`

    `void sayHello() { std::cout << "Hello from MyClass!\\\\n"; }`

`};`



`int main() {`

    `std::unique\\\_ptr<MyClass> ptr = std::make\\\_unique<MyClass>();`

    `ptr->sayHello();`



    // No need to manually delete — destructor is called automatically

    `return 0;`

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

`    std::shared\\\_ptr<Node> next;`

`    std::weak\\\_ptr<Node> prev; // prevents cyclic reference`



`    Node(int val) : value(val) {}`

`};`



`int main() {`

 `   auto node1 = std::make\\\_shared<Node>(1);`

  `  auto node2 = std::make\\\_shared<Node>(2);`



`    node1->next = node2;`

 `   node2->prev = node1; // weak\\\_ptr avoids memory leak`



`    std::cout << "Node1 value: " << node1->value << "\\\\n";`

 `   std::cout << "Node2 value: " << node2->value << "\\\\n";`

`}`



\# Key Points



    std::unique\_ptr → sole ownership, lightweight, best for exclusive resources.



    std::shared\_ptr → multiple owners, uses reference counting.



    std::weak\_ptr → observes a shared\_ptr without affecting its lifetime.



    Prefer std::make\_unique / std::make\_shared over new for exception safety.



\# Example Usage Summary



`int main() {`

    `auto uptr = std::make\\\_unique<int>(42);   // unique\\\_ptr`

    `auto sptr = std::make\\\_shared<int>(100);  // shared\\\_ptr`

    `std::weak\\\_ptr<int> wptr = sptr;          // weak\\\_ptr`



    `std::cout << \\\*uptr << " " << \\\*sptr << "\\\\n"; // Output: 42 100`

`}`

