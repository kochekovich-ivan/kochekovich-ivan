# Iterators


### Types of Iterators

1. **Input Iterator** – Read-only access, one-pass, forward movement.
2. **Output Iterator** – Write-only access, one-pass, forward movement.
3. **Forward Iterator** – Read/write access, multi-pass, forward movement.
4. **Bidirectional Iterator** – Can move both forward and backward.
5. **Random Access Iterator** – Supports full pointer arithmetic (used by vectors, arrays, deque).

### Basic Syntax
``` C++
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> nums = {10, 20, 30, 40};

    // Declaring an iterator
    vector<int>::iterator it;

    for (it = nums.begin(); it != nums.end(); ++it) {
        cout << *it << " ";  // Dereferencing to access value
    }
    return 0;
}
```
### Important Iterator Functions

- **begin()** – Returns iterator to the first element.
- **end()** – Returns iterator to the element past the last one (not valid for dereferencing).
- **rbegin()** – Returns reverse iterator to the last element.
- **rend()** – Returns reverse iterator to one element before the first.
- **cbegin() / cend()** – Return constant iterators (read-only).
- **crbegin() / crend()** – Return constant reverse iterators.

### Reverse Iterators Example
``` C++
#include <iostream>
#include <vector>
using namespace std;

int main() {
    vector<int> nums = {1, 2, 3, 4, 5};

    for (vector<int>::reverse_iterator rit = nums.rbegin(); rit != nums.rend(); ++rit) {
        cout << *rit << " ";  // Prints elements in reverse order
    }
    return 0;
}
```
### Operations on Iterators (for Random Access Containers)

If the container supports random access iterators (like vector or array):

- it + n → Move iterator forward by n positions.
- it - n → Move iterator backward by n positions.
- it1 - it2 → Returns distance between two iterators.
- it[n] → Access element like array indexing.
- ++it / it++ → Move to next element.
- --it / it-- → Move to previous element (bidirectional iterators).

### Advantages of Iterators

- Provide a uniform way to traverse containers.
- Work with STL algorithms like sort, find, copy, etc.
- Decouple traversal logic from container implementation.

### Common Use with Algorithms
``` C++
#include <iostream>
#include <vector>
#include <algorithm>
using namespace std;

int main() {
    vector<int> nums = {10, 30, 20, 50, 40};

    sort(nums.begin(), nums.end());

    for (auto it = nums.begin(); it != nums.end(); ++it) {
        cout << *it << " ";
    }
    return 0;
}
```
## Key Points / Notes

- Iterators work like smart pointers that abstract container internals.
- Dereference (*) to access the value.
- `end()` points past the last element — do not dereference it.
- Use const iterators (cbegin/cend) when you don't need to modify elements.
- Random access iterator operations are available only for containers like vector, deque, and array.

## Applications / Use Cases

- Traversing any STL container generically.
- Using STL algorithms (sort, find, count, etc.).
- Modifying or reading container elements without exposing internal structure.
