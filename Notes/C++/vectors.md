# Vectors


### Key Characteristics

- Stored in **contiguous memory** (like arrays).
- Can **resize dynamically** as elements are added or removed.
- Support **random access** (constant time access to elements by index).
- Provide built-in functions for insertion, deletion, and traversal.

### Syntax

To use vectors, include the `<vector>` header and use the `std::vector` class.
``` C++
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> numbers;  // Declare a vector of integers
    numbers.push_back(10);
    numbers.push_back(20);
    numbers.push_back(30);

    cout << "First element: " << numbers[0] << endl;
    return 0;
}
```
### Common Member Functions

- **push_back(value)** – Adds an element to the end of the vector.
- **pop_back()** – Removes the last element.
- **size()** – Returns the number of elements.
- **empty()** – Returns true if the vector is empty.
- **clear()** – Removes all elements.
- **at(index)** – Access element at a given index with bounds checking.
- **front() / back()** – Access the first or last element.
- **insert(iterator, value)** – Insert at a specific position.
- **erase(iterator)** – Remove an element at a specific position.
- **resize(n)** – Change the size of the vector.
- **capacity()** – Returns how many elements the vector can hold before it needs to allocate more memory.

### Iterating Through a Vector
``` C++
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> nums = {1, 2, 3, 4, 5};

    // Using index
    for (int i = 0; i < nums.size(); i++) {
        cout << nums[i] << " ";
    }

    // Using iterator
    for (vector<int>::iterator it = nums.begin(); it != nums.end(); ++it) {
        cout << *it << " ";
    }

    // Using range-based for loop
    for (int x : nums) {
        cout << x << " ";
    }
    return 0;
}
```
### Advantages of Vectors

- Automatic memory management.
- Easy to use compared to raw arrays.
- Provide many helpful member functions for manipulation.
- Safe access with `.at()` (throws out_of_range exception).

### Limitations

- Slightly slower than raw arrays for some operations due to overhead.
- When capacity is exceeded, reallocation occurs (costly operation).

## Applications / Use Cases

- Storing collections of data where size can change dynamically.
- Implementing stacks, queues, and other data structures.
- Situations where you need random access and automatic memory handling.

## Key Points / Notes

- Always include `<vector>` before using vectors.
- Vectors store elements in contiguous memory, so pointer arithmetic works like arrays.
- Use reserve(n) to preallocate memory when the number of elements is known in advance to improve performance.
