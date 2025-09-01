\# What is a linked list?



A singly linked list is a linear data structure consisting of nodes.

Each node contains:



data – the value,



next – a pointer to the next node in the list.



The last node points to nullptr, which means the end of the list.



Unlike arrays, linked lists:



do not require contiguous memory,



allow fast insertion/deletion at the beginning or end,



but have slower access to elements (need to traverse).



\# Node structure

`struct Node {`

&nbsp;   `int data;`

&nbsp;   `Node\* next;`

&nbsp;   `Node(int value) : data(value), next(nullptr) {}`

`};`



\# LinkedList class (basic implementation)

`class LinkedList {`

`private:`

&nbsp;   `Node\* head = nullptr;`

&nbsp;   `Node\* tail = nullptr;`

&nbsp;   `unsigned int counter{0};`



`public:`

&nbsp;   `void push\_back(int value);     // add element to the end`

&nbsp;   `void print\_all\_el();           // print all elements`

&nbsp;   `unsigned int size();           // return size`

&nbsp;   `~LinkedList();                 // destructor to free memory`

`};`



\# Implemented methods



push\_back(int value) – adds an element to the end of the list.



print\_all\_el() – traverses the list and prints all elements.



size() – returns the number of elements.



~LinkedList() – destructor, frees all allocated memory.



\# Example usage
`int main() {`

&nbsp;   `LinkedList my\_list;`

&nbsp;   `my\_list.push\_back(10);`

&nbsp;   `my\_list.push\_back(15);`

&nbsp;   `my\_list.print\_all\_el();   // Output: 10 15`

&nbsp;   `cout << my\_list.size();   // Output: 2`

&nbsp;   `return 0;`

`}`











