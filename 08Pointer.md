
# Pointers


## Declaring and Initialising

Pointers are a fundamental concept in the C programming language. They allow you to manipulate memory addresses directly, giving you a lot of control and flexibility when working with data.

A pointer is simply a variable that stores the memory address of another variable. The memory address can be thought of as the location of a particular piece of data in the computer's memory. To declare a pointer in C, you use the "*" operator, for example:


```c
int x = 5;
int *ptr = &x;
```


Here, "ptr" is a pointer to an "int" variable, and "&x" is the memory address of the variable "x". The "&" operator is used to get the memory address of a variable.

You can use the "*" operator to access the value stored at the memory address stored in a pointer. For example:


```c
int x = 5;
int *ptr = &x;
printf("Value of x: %d\n", x);
printf("Value stored at the memory address pointed by ptr: %d\n", *ptr);
```


This will output:


```c
Value of x: 5
Value stored at the memory address pointed by ptr: 5
```


In C programming, pointers are useful in a variety of ways, including:



* Pointers allow you to allocate memory dynamically at runtime rather than having to define all variables at compile time.
* Pointers can be used as function arguments to pass variables by reference, which allows the function to modify the original variable.
* Pointers are the building blocks of linked data structures such as linked lists and trees.

Overall, pointers are a useful tool in C programming, but they can be dangerous if not used properly. Understanding pointer usage is critical for writing efficient and secure C code.


## Pointer Arithmetics

The process of performing arithmetic operations on pointers in C is known as pointer arithmetic. Pointers are variables that hold memory addresses, and pointer arithmetic allows you to manipulate the memory addresses that pointers hold.

Pointer arithmetic is divided into two types: incrementing and decrementing pointers and adding and subtracting integers from pointers.


### Incrementing and Decrementing Pointers

Using the ++ and -- operators, you can increment or decrement a pointer by a specified number of bytes. The amount by which the pointer is incremented or decremented depends on the data type that the pointer points to. For example, increasing a pointer to an int by one increases the pointer by four bytes (the size of an int), whereas increasing a pointer to a char by one byte (the size of a char).


### Adding and Subtracting Integers from Pointers

You can also use the + and - operators to add or subtract an integer value from a pointer. The operation's outcome is determined by the data type to which the pointer points. Adding 3 to a pointer to an int, for example, increases the pointer by 12 bytes (3 * int size), whereas adding 3 to a pointer to a char increases the pointer by 3 bytes (3 * char size).

It should be noted that pointer arithmetic is performed in units of the size of the data type to which the pointer points, not in units of the actual data stored at the memory location. This means that incrementing a pointer by one does not always move it to the next data item, but rather to the next memory location of the same size as the data type to which the pointer points.

Pointer arithmetic is a powerful C feature that lets you manipulate memory addresses, but it should be used with caution. Incorrect pointer arithmetic can cause memory access errors and unpredictability in your programme.

Here's an example of pointer arithmetic in C:


```c
#include <stdio.h>

int main() {
   int arr[5] = {10, 20, 30, 40, 50};
   int *ptr;

   // Point the pointer to the first element of the array
   ptr = arr;

   // Increment the pointer to point to the next element
   ptr++;

   // Access the value at the new memory location
   printf("Value at the new memory location: %d\n", *ptr);

   // Add 2 to the pointer to point to the third element
   ptr = ptr + 2;

   // Access the value at the new memory location
   printf("Value at the new memory location: %d\n", *ptr);

   return 0;
}
```


The ptr pointer is first set to point to the first element of the arr array in this example. Using the ptr++ operator, the ptr pointer is then incremented to point to the next element in the array. The *ptr expression is then used to access the value at the new memory location.

The ptr pointer is then incremented by 8 bytes (2 * the size of an int) by using the ptr + 2 expression. Finally, the *ptr expression is used to access the value at the new memory location.

When you run this programme, you'll get the following output:


```c
Value at the new memory location: 20
Value at the new memory location: 30
```


This example shows how pointer arithmetic can be used to manipulate memory addresses and access data stored in different memory locations.


## Pointer and Functions

To pass data between the caller and the called function, pointers can be used in conjunction with functions. This allows you to change data in the scope of the caller from within the called function.

Passing data to a function with pointers can be accomplished in two ways: pass-by-reference and pass-by-pointer.


### Pass-by-Reference

You can pass a reference to a variable to a function using a pointer. This allows the called function to access and modify the original variable in the caller's scope. To pass a variable by reference, you simply pass a pointer to the variable to the function. Here's an example:


```c
#include <stdio.h>

void swap(int *a, int *b) {
   int temp = *a;
   *a = *b;
   *b = temp;
}

int main() {
   int x = 10, y = 20;
   printf("Before swapping: x = %d, y = %d\n", x, y);
   swap(&x, &y);
   printf("After swapping: x = %d, y = %d\n", x, y);

   return 0;
}
```


In this example, the swap function takes two pointers to int as arguments. The values stored at the memory locations pointed to by these pointers are then swapped within the function. Note that the & operator is used to pass the address of the x and y variables to the function.


## Pass-by-Pointer

Another way to pass data to a function using pointers is to pass a pointer to the function. This allows the called function to access the original data stored at the memory location pointed to by the pointer, but not to modify the pointer itself. Here's an example:


```c
#include <stdio.h>

void print_array(int *arr, int size) {
   int i;
   for (i = 0; i < size; i++) {
      printf("%d ", arr[i]);
   }
   printf("\n");
}

int main() {
   int arr[] = {10, 20, 30, 40, 50};
   int size = sizeof(arr) / sizeof(arr[0]);

   printf("Array elements: ");
   print_array(arr, size);

   return 0;
}
```


In this example, the print_array function takes a pointer to int and an int as arguments. The function uses the pointer to access and print the elements of the array passed to it. Note that the pointer itself is not modified within the function.

Using pointers with functions in this way can be very useful for passing large amounts of data between functions, as it avoids the need to make copies of the data, which can be time-consuming and memory-intensive.


## Pointers and Arrays

Pointers and arrays are closely related in C, and a pointer can often be used to manipulate an array.

An array is essentially a block of memory that holds a collection of elements of the same data type. The name of an array is a constant pointer that points to the first element of the array. This means that you can use a pointer to access elements of an array by using pointer arithmetic.

Here's an example:


```c
#include <stdio.h>

int main() {
   int arr[] = {10, 20, 30, 40, 50};
   int *ptr = arr;

   int i;
   for (i = 0; i < 5; i++) {
      printf("%d ", *ptr);
      ptr++;
   }
   printf("\n");

   return 0;
}
```


In this example, the ptr pointer is assigned the value of the arr array, which is a pointer to the first element of the array. The ptr pointer is then used to access and print the elements of the array using pointer arithmetic (ptr++).

Another advantage of using pointers with arrays is that you can pass arrays to functions as pointers. This allows you to modify the elements of an array within the function and have those changes reflected in the caller's scope.

Here's an example:


```c
#include <stdio.h>

void modify_array(int *arr, int size) {
   int i;
   for (i = 0; i < size; i++) {
      arr[i] *= 2;
   }
}

int main() {
   int arr[] = {10, 20, 30, 40, 50};
   int size = sizeof(arr) / sizeof(arr[0]);

   printf("Before modification: ");
   int i;
   for (i = 0; i < size; i++) {
      printf("%d ", arr[i]);
   }
   printf("\n");

   modify_array(arr, size);

   printf("After modification: ");
   for (i = 0; i < size; i++) {
      printf("%d ", arr[i]);
   }
   printf("\n");

   return 0;
}
```


In this example, the modify_array function takes a pointer to int and an int as arguments. The function uses the pointer to access and modify the elements of the array passed to it. Note that the changes made within the function are reflected in the caller's scope, even though the function only receives a pointer to the array, not the actual array itself.


## Pointer to a Pointer

A pointer to a pointer (double pointer) is a type of pointer that stores the memory address of another pointer. In other words, it's a pointer that points to another pointer.

Here's an example of how to declare and use a double pointer in C:


```c
int x = 5;
int *ptr1 = &x;
int **ptr2 = &ptr1;
```


In this example, `ptr1` is a pointer to an `int `variable, and `ptr2 `is a pointer to a pointer to an int. The value of `ptr2 `is the memory address of `ptr1`, and the value stored at the memory address pointed to by `ptr2 `is the value of `ptr1`, which is the memory address of x.

