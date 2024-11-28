# Data types and its size
| Data Type    | Size (bytes) | Description                                    |
|--------------|--------------|------------------------------------------------|
| `char`       | 1            | Character data type.                           |
| `bool`       | 1            | Boolean data type.                             |
| `int`        | 4            | Integer data type.                             |
| `float`      | 4            | Floating-point data type.                      |
| `double`     | 8            | Double precision floating-point data type.     |
| `wchar_t`    | 2 or 4       | Wide character data type.                      |
| `short`      | 2            | Short integer data type.                       |
| `long`       | 4 or 8       | Long integer data type.                        |
| `long long`  | 8            | Long long integer data type.                   |
| `unsigned int`| 4            | Unsigned integer data type.                    |

- Keep in mind, these sizes can vary based on the compiler and the architecture you're working on, but these values are commonly seen.
---

# Array

### **What is an Array?**
An array in C++ is a collection of elements, all of the same type, placed in contiguous memory locations. It allows you to store multiple values in a single variable, instead of declaring separate variables for each value.

### **Declaration of Arrays**
To declare an array in C++, you specify the type of its elements and the number of elements required by an array as follows:

```cpp
int arr[10]; // array of 10 integers
```

### **Initialization of Arrays**
You can initialize an array at the time of declaration:

```cpp
int arr[5] = {1, 2, 3, 4, 5};
```

If you don’t initialize an array, elements will have garbage values (undefined).

### **Accessing Array Elements**
Array elements are accessed using their index. Remember that array indexing starts from 0:

```cpp
int firstElement = arr[0]; // accessing first element
int thirdElement = arr[2]; // accessing third element
```

### **Multidimensional Arrays**
C++ allows multidimensional arrays. Here's how you can declare and initialize them:

```cpp
int arr[2][3] = {{1, 2, 3}, {4, 5, 6}};
```

### **Size of an Array**
To get the size of an array, you can use the `sizeof` operator:

```cpp
int arrSize = sizeof(arr) / sizeof(arr[0]);
```

### **Iterating Over Arrays**
You can use loops to iterate over array elements:

```cpp
for(int i = 0; i < 5; i++) {
    cout << arr[i] << " ";
}
```

### **Common Operations with Arrays**
Here are some common operations you can perform on arrays:

1. **Insertion**: Adding a new element.
2. **Deletion**: Removing an element.
3. **Searching**: Finding a specific element.
4. **Sorting**: Ordering elements (ascending or descending).

### **Advantages of Arrays**
- Fixed-size: Memory allocation is static and efficient.
- Random access: O(1) access time for elements.

### **Disadvantages of Arrays**
- Fixed-size: Can’t resize dynamically once defined.
- Contiguous memory allocation: Can cause memory wastage if array is not fully utilized.

### **Examples**

#### Single-dimensional Array:
```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {1, 2, 3, 4, 5};
    for(int i = 0; i < 5; i++) {
        cout << arr[i] << " ";
    }
    return 0;
}
```

#### Multidimensional Array:
```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[2][3] = {{1, 2, 3}, {4, 5, 6}};
    for(int i = 0; i < 2; i++) {
        for(int j = 0; j < 3; j++) {
            cout << arr[i][j] << " ";
        }
        cout << endl;
    }
    return 0;
}
```

### **Conclusion**
Arrays are fundamental data structures in C++ that provide a simple and efficient way to store multiple elements. They are crucial for understanding more complex data structures and algorithms.

