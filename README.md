# C-Questions
# 📘 C++ Pointer & Memory Assignment  
**CSE 2025**

This document contains complete solutions to all questions given by the instructor.  
All programs are written strictly in **C++** and formatted for academic submission.

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

# Question 2
Write a function square(int) and call it:
Normally
Using a function pointer
Copy code
```
Cpp
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
Copy code
Cpp
```
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
Copy code
Cpp
```
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
Copy code
Cpp
```
int x = 5;
int *p = &x;
*p = 10;
cout << x;
Output:
Copy code
```
10

# Question 6
What will be the output:
Copy code
Cpp
```
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
Copy code
Cpp
```
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
Copy code
Cpp
```
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
Copy code
Cpp
```
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
Copy code
Cpp
```
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