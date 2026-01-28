# C-Questions

---

## Question 1

**Write a C++ program that:**
- Declares one global variable  
- Declares one local variable inside `main()`  
- Dynamically allocates one integer using `new`  
- Print the addresses of all three and identify which memory region each belongs to  

```cpp
#include <iostream>
using namespace std;

int globalVar = 10;   // Global / Static memory

int main() {
    int localVar = 20;              // Stack memory
    int *dynamicVar = new int(30);  // Heap memory

    cout << "Global Variable Address (Static): " << &globalVar << endl;
    cout << "Local Variable Address (Stack): " << &localVar << endl;
    cout << "Dynamic Variable Address (Heap): " << dynamicVar << endl;

    delete dynamicVar;
    return 0;
}
```
# Question 2
Write a function square(int) and call it:
Normally
Using a function pointer
Copy code

```cpp
#include <iostream>
using namespace std;

int square(int x) {
    return x * x;
}

int main() {
    cout << "Normal Call: " << square(5) << endl;

    int (*funcPtr)(int) = square;
    cout << "Function Pointer Call: " << funcPtr(5) << endl;

    return 0;
}
```
# Question 3
Write a program to print:
Value of a variable
Address of the variable
Value stored in the pointer

```cpp
#include <iostream>
using namespace std;

int main() {
    int x = 10;
    int *p = &x;

    cout << "Value of variable: " << x << endl;
    cout << "Address of variable: " << &x << endl;
    cout << "Value stored in pointer: " << p << endl;

    return 0;
}
```
# Question 4
Write a program where a pointer stores the address of another variable and copies its value into a third variable using dereferencing.

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 50;
    int *p = &a;
    int b = *p;

    cout << "Value of a: " << a << endl;
    cout << "Copied value in b: " << b << endl;

    return 0;
}
```
# Question 5
What will be the output:

```cpp
int x = 5;
int *p = &x;
*p = 10;
cout << x;
Output:


10
```
# Question 6
What will be the output:
```cpp
int a = 1, b = 2;
int *p = &a;
p = &b;
*p = 5;
cout << a << " " << b;
Output:
Copy code

1 5
```
# Question 7
What will be the output:

```cpp
int x = 10;
int *p = &x;
int **pp = &p;
**pp = 20;
cout << x;
Output:
Copy code

20
```
# Question 8
What will be the output:

```cpp
int a[5] = {2,4,6,8,10};
int *p = a;
cout << *p++ << " ";
cout << *p;
Output:
Copy code

2 4
```
# Question 9
Write a program to swap two numbers using pointers.


```cpp
#include <iostream>
using namespace std;

void swapNumbers(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

int main() {
    int x = 5, y = 10;
    swapNumbers(&x, &y);

    cout << "After Swapping: x = " << x << ", y = " << y;
    return 0;
}
```
# Question 10
Implement a simple dynamic integer variable that:
Is created using new
Modified through a pointer
Properly deleted

```cpp
#include <iostream>
using namespace std;

int main() {
    int *p = new int(10);

    cout << "Initial Value: " << *p << endl;

    *p = 50;
    cout << "Modified Value: " << *p << endl;

    delete p;
    p = nullptr;

    return 0;
}
```



## 🟢 Question 1: Read and Display Elements of an Array

### Problem Statement  
Write a C++ program to read and display elements of an array.

```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "Enter number of elements: ";
    cin >> n;

    int arr[n];

    cout << "Enter elements:\n";
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    cout << "Array elements are:\n";
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }

    return 0;
}


---

🟢 Question 2: Find the Sum of All Elements in an Array

Problem Statement

Write a C++ program to find the sum of all elements in an array.
```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    int sum = 0;

    cout << "Enter number of elements: ";
    cin >> n;

    int arr[n];

    cout << "Enter elements:\n";
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
        sum += arr[i];
    }

    cout << "Sum of array elements: " << sum;

    return 0;
}

```
---

🟢 Question 3: Copy One Array into Another

Problem Statement

Write a C++ program to copy one array into another.
```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "Enter number of elements: ";
    cin >> n;

    int arr1[n], arr2[n];

    cout << "Enter elements of first array:\n";
    for (int i = 0; i < n; i++) {
        cin >> arr1[i];
        arr2[i] = arr1[i];
    }

    cout << "Copied array elements:\n";
    for (int i = 0; i < n; i++) {
        cout << arr2[i] << " ";
    }

    return 0;
}

```
---

🟢 Question 4: Print Array Elements at Even Index Positions

Problem Statement

Write a C++ program to print array elements at even index positions.
```cpp
#include <iostream>
using namespace std;

int main() {
    int n;
    cout << "Enter number of elements: ";
    cin >> n;

    int arr[n];

    cout << "Enter elements:\n";
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    cout << "Elements at even index positions:\n";
    for (int i = 0; i < n; i += 2) {
        cout << arr[i] << " ";
    }

    return 0;
}
```

---

🟢 Question 5: Read and Display a 2D Array (Matrix)

Problem Statement

Write a C++ program to read and display a 2D array (matrix).
```cpp
#include <iostream>
using namespace std;

int main() {
    int rows, cols;
    cout << "Enter number of rows and columns: ";
    cin >> rows >> cols;

    int matrix[rows][cols];

    cout << "Enter matrix elements:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cin >> matrix[i][j];
        }
    }

    cout << "Matrix:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cout << matrix[i][j] << " ";
        }
        cout << endl;
    }

    return 0;
}

```
---

🟢 Question 6: Print Matrix Elements in Row-Wise Order

Problem Statement

Write a C++ program to print all elements of a matrix in row-wise order.
```cpp
#include <iostream>
using namespace std;

int main() {
    int rows, cols;
    cout << "Enter rows and columns: ";
    cin >> rows >> cols;

    int matrix[rows][cols];

    cout << "Enter matrix elements:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cin >> matrix[i][j];
        }
    }

    cout << "Row-wise order:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cout << matrix[i][j] << " ";
        }
    }

    return 0;
}

```
---

🟢 Question 7: Print Matrix Elements in Column-Wise Order

Problem Statement

Write a C++ program to print all elements of a matrix in column-wise order.
```cpp
#include <iostream>
using namespace std;

int main() {
    int rows, cols;
    cout << "Enter rows and columns: ";
    cin >> rows >> cols;

    int matrix[rows][cols];

    cout << "Enter matrix elements:\n";
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            cin >> matrix[i][j];
        }
    }

    cout << "Column-wise order:\n";
    for (int j = 0; j < cols; j++) {
        for (int i = 0; i < rows; i++) {
            cout << matrix[i][j] << " ";
        }
    }

    return 0;
}

```
---
