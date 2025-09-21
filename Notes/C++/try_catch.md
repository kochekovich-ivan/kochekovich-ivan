The general flow is:

1. Code that might throw an exception is placed inside a `try` block.
2. If an exception is thrown using `throw`, control jumps to the matching `catch` block.
3. `catch` handles the exception and prevents program crash.

### Syntax
``` C++
#include <iostream>
using namespace std;

int main() {
    try {
        int a = 10, b = 0;
        if (b == 0) {
            throw "Division by zero error!";
        }
        cout << "Result: " << a / b << endl;
    }
    catch (const char* msg) {
        cout << "Exception caught: " << msg << endl;
    }

    return 0;
}
```
### Multiple Catch Blocks

You can have multiple `catch` blocks to handle different types of exceptions.
``` C++
try {
    throw 10;
}
catch (int x) {
    cout << "Caught an integer: " << x << endl;
}
catch (const char* msg) {
    cout << "Caught a string: " << msg << endl;
}
```
### Catch-All Handler

Use `catch(...)` to handle any exception type when the exact type is not known.
``` C++
try {
    throw 3.14;
}
catch (...) {
    cout << "Caught an unknown exception" << endl;
}
```
### Nested try-catch

You can nest try-catch blocks to handle errors at multiple levels.
``` C++
try {
    try {
        throw "Inner exception";
    }
    catch (const char* e) {
        cout << "Inner catch: " << e << endl;
        throw;  // rethrow exception to outer block
    }
}
catch (...) {
    cout << "Outer catch: handled rethrown exception" << endl;
}
```
## Key Points / Notes

- `throw` can be used to throw any type (int, char, class objects, etc.).
- Always catch exceptions by reference if they are objects (to avoid copying).
- If no matching `catch` is found, the program calls `std::terminate()`.
- Use `catch(...)` as a last resort to handle unexpected errors.
- Avoid overusing exceptions for normal program flow — they are meant for error handling.

## Applications / Use Cases

- Handling runtime errors like division by zero, file I/O errors, memory allocation failures.
- Writing robust code that doesn't crash when exceptions occur.
- Implementing custom exception classes for domain-specific errors.
