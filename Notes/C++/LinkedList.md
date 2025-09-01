# Linked List

## What is a linked list?

A **singly linked list** is a linear data structure consisting of nodes.  

Each node contains:  
- data – the value  
- next – a pointer to the next node in the list  

The last node points to nullptr, indicating the end of the list.  

**Differences from arrays:**  
- Do **not** require contiguous memory  
- Allow **fast insertion/deletion** at the beginning or end  
- Slower element access (traversal required)

## Node structure

struct Node {  
  int data;  
  Node* next;  
  Node(int value) : data(value), next(nullptr) {}  
};

## LinkedList class (basic implementation)

class LinkedList {  
private:  
  Node* head = nullptr;  
  Node* tail = nullptr;  
  unsigned int counter{0};  

public:  
  void push_back(int value);     // add element to the end  
  void print_all_el();           // print all elements  
  unsigned int size();           // return size  
  ~LinkedList();                 // destructor to free memory  
};

## Implemented methods

- push_back(int value) – adds an element to the **end** of the list  
- print_all_el() – traverses the list and prints all elements  
- size() – returns the number of elements  
- ~LinkedList() – destructor, frees all allocated memory

## Example usage

int main() {  
  LinkedList my_list;  
  my_list.push_back(10);  
  my_list.push_back(15);  
  my_list.print_all_el();   // Output: 10 15  
  cout << my_list.size();   // Output: 2  
  return 0;  
}

