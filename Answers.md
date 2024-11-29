
# 5-Mark Answers:

## 1. Menu-Driven Program Using Switch Case
A menu-driven program presents options to users and performs specific tasks based on their choices using a switch case.

**Example Code:**

```c
#include <stdio.h>
int main() {
    int choice, a, b;
    printf("Choose an operation: 1.Add 2.Subtract 3.Multiply 4.Divide\n");
    scanf("%d", &choice);
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    switch (choice) {
        case 1: printf("Sum: %d\n", a + b); break;
        case 2: printf("Difference: %d\n", a - b); break;
        case 3: printf("Product: %d\n", a * b); break;
        case 4: if (b != 0) printf("Quotient: %.2f\n", (float)a / b);
                else printf("Division by zero is not allowed.\n");
                break;
        default: printf("Invalid choice.\n");
    }
    return 0;
}
```

---

## 2. Library Management System Using Structure
A structure groups related data. In a library management system, it can store book ID, title, author, and availability.

**Example Structure:**

```c
struct Book {
    int bookID;
    char title[50];
    char author[50];
    int isAvailable;
};
void displayBook(struct Book b) {
    printf("ID: %d, Title: %s, Author: %s, Available: %s\n", 
           b.bookID, b.title, b.author, b.isAvailable ? "Yes" : "No");
}
```

---

## 3. Grade Student System Using Nested if or if-else
**Program:**

```c
#include <stdio.h>
int main() {
    int score;
    printf("Enter the score: ");
    scanf("%d", &score);
    if (score >= 90)
        printf("Grade: A\n");
    else if (score >= 80)
        printf("Grade: B\n");
    else if (score >= 70)
        printf("Grade: C\n");
    else if (score >= 60)
        printf("Grade: D\n");
    else
        printf("Grade: F\n");
    return 0;
}
```

---

## 4. Difference Between Structure and Union

- **Structures** store all members in separate memory locations.
- **Unions** share the same memory for all members.
- Structures allow simultaneous access to all members, but unions only provide access to one member at a time.

---

## 5. Difference Between malloc and calloc

- **malloc** allocates uninitialized memory, while **calloc** allocates zero-initialized memory.
- calloc takes two arguments: number of blocks and block size, while malloc takes one: total size in bytes.

---

# 10-Mark Answers:

## 1. Range of Palindrome, Prime, Perfect Numbers
**Program Outline:**
- Check for palindrome: Reverse the number and compare.
- Check for prime: Test divisors up to the square root of the number.
- Check for perfect number: Sum all divisors and compare with the number.

---

## 2. Largest Number Using Function and Pointer
**Program:**

```c
#include <stdio.h>
int largest(int *x, int *y, int *z) {
    if (*x > *y && *x > *z) return *x;
    else if (*y > *z) return *y;
    else return *z;
}
int main() {
    int a, b, c;
    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);
    printf("Largest number: %d\n", largest(&a, &b, &c));
    return 0;
}
```

---

## 3. Multi-Dimensional Array

**Concept:** Arrays with more than one dimension, e.g., 2D arrays for matrices.

**Matrix Addition Example:**

```c
#include <stdio.h>
int main() {
    int a[2][2] = {{1, 2}, {3, 4}}, b[2][2] = {{5, 6}, {7, 8}}, c[2][2];
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            c[i][j] = a[i][j] + b[i][j];
            printf("%d ", c[i][j]);
        }
        printf("\n");
    }
    return 0;
}
```

---

## 4. Static Variables: Local and Global
**Program:**

```c
#include <stdio.h>
void demo() {
    static int count = 0; // Static local variable
    count++;
    printf("Count: %d\n", count);
}
int main() {
    for (int i = 0; i < 3; i++)
        demo();
    return 0;
}
```

---

## 5. Flowchart & Algorithm

**Algorithm:**

1. Start.
2. Input n.
3. Initialize fact = 1.
4. For each i from 1 to n, multiply fact by i.
5. Output fact.
6. Stop.

**Flowchart:** Use a decision box for the loop and a process box for calculations.
