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

    `int data;`

    `Node\\\* next;`

    `Node(int value) : data(value), next(nullptr) {}`

`};`



\# LinkedList class (basic implementation)

`class LinkedList {`

`private:`

    `Node\\\* head = nullptr;`

    `Node\\\* tail = nullptr;`

    `unsigned int counter{0};`



`public:`

    `void push\\\_back(int value);     // add element to the end`

    `void print\\\_all\\\_el();           // print all elements`

    `unsigned int size();           // return size`

    `~LinkedList();                 // destructor to free memory`

`};`



\# Implemented methods



push\_back(int value) – adds an element to the end of the list.



print\_all\_el() – traverses the list and prints all elements.



size() – returns the number of elements.



~LinkedList() – destructor, frees all allocated memory.



\# Example usage
`int main() {`

    `LinkedList my\\\_list;`

    `my\\\_list.push\\\_back(10);`

    `my\\\_list.push\\\_back(15);`

    `my\\\_list.print\\\_all\\\_el();   // Output: 10 15`

    `cout << my\\\_list.size();   // Output: 2`

    `return 0;`

`}`

