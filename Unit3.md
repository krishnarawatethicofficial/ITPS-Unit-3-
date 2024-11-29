
# Unit 3 - C Programming Topics

## 1. Basics of Structures in C
- Structures are user-defined data types that group variables of different types into a single unit.
- Defined using the `struct` keyword.
- Example:
```c
struct Student {
    int id;
    char name[50];
};
```
- Accessing structure members:
```c
struct Student s1;
s1.id = 1;
strcpy(s1.name, "John");
```

## 2. Nested Structures in C
- Structures can be nested, i.e., one structure can be a member of another structure.
- Example:
```c
struct Address {
    char city[20];
    int pin;
};
struct Student {
    int id;
    struct Address addr;
};
```
- Accessing nested members:
```c
struct Student s1;
strcpy(s1.addr.city, "New York");
s1.addr.pin = 12345;
```

## 3. Array of Structures in C
- An array of structures is a collection of structure variables.
- Example:
```c
struct Student students[10];
students[0].id = 1;
strcpy(students[0].name, "Alice");
```

## 4. Use of Structures with Functions and Pointers
- Structures can be passed to functions by value or reference (using pointers).
- Example (passing by reference):
```c
void display(struct Student *s) {
    printf("ID: %d, Name: %s", s->id, s->name);
}
```

## 5. Concept of Pointer and Pointer to Pointer in C
- A pointer stores the address of a variable, and a pointer to pointer stores the address of another pointer.
- Example:
```c
int x = 10, *p = &x, **pp = &p;
printf("Value of x: %d", **pp);
```

## 6. Pointer Arithmetic in C
- Operations like increment, decrement, addition, and subtraction can be performed on pointers.
- Example:
```c
int arr[5] = {1, 2, 3, 4, 5};
int *p = arr;
p++; // Now points to arr[1]
```

## 7. Pointer with Arrays and Functions
- Arrays can be accessed using pointers.
- Example:
```c
int arr[5] = {1, 2, 3, 4, 5};
int *p = arr;
for (int i = 0; i < 5; i++) {
    printf("%d ", *(p + i));
}
```

## 8. Storage Classes in C
- Determines the scope, lifetime, and visibility of variables.
    - `auto`: Default for local variables.
    - `register`: Stored in CPU registers for fast access.
    - `static`: Retains its value between function calls.
    - `extern`: Refers to a global variable.
- Example:
```c
static int count = 0; // Retains value across function calls
```

## 9. Dynamic Memory Allocation
- Dynamic memory management functions:
    - `malloc()`: Allocates memory dynamically.
    - `calloc()`: Allocates memory and initializes it to zero.
    - `free()`: Frees allocated memory.
    - `realloc()`: Resizes allocated memory.
- Example:
```c
int *ptr = (int *)malloc(5 * sizeof(int));
free(ptr);
```

## 10. Program Based on Pointer
- Example demonstrating pointer usage:
```c
#include <stdio.h>
void swap(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}
int main() {
    int x = 10, y = 20;
    swap(&x, &y);
    printf("x: %d, y: %d", x, y);
    return 0;
}
```
