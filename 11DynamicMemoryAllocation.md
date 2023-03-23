

# Dynamic Memory Allocation

In C, dynamic memory allocation allows you to allocate and deallocate memory dynamically at runtime rather than statically at compile time. This gives you more control and flexibility over memory usage in your programme.


## Malloc() and Calloc()

The C functions malloc() and calloc() allow you to allocate memory dynamically. Malloc() allocates a block of memory of a given size, whereas calloc() allocates a block of memory for an array of a given size.

Here's an example of using malloc():


```c
int *ptr;
ptr = (int *) malloc(sizeof(int));
```


This code uses malloc() to allocate a block of memory for an integer and then assigns the pointer to ptr. If malloc() is unable to allocate the memory, it will return NULL. 

Here's an example of using calloc():


```c
int *ptr;
ptr = (int *) calloc(10, sizeof(int));
```


Using calloc(), this code allocates a block of memory for an array of ten integers and assigns the pointer to ptr. If calloc() fails to allocate memory, it returns NULL.


## Realloc() and Free()

Realloc() and free() are C functions that allow you to modify and deallocate dynamically allocated memory. realloc() resizes the memory block to a new size, whereas free() frees the memory block.

Here's an example of how to use realloc():


```c
int *ptr;
ptr = (int *) malloc(10 * sizeof(int));

// resize the memory block to 20 integers
ptr = (int *) realloc(ptr, 20 * sizeof(int));
```


This code first uses malloc() to allocate a block of memory for an array of ten integers and then assigns the pointer to ptr. The memory block is then resized to a new size of 20 integers using realloc().

Here's an example of how to use free():


```c
int *ptr;
ptr = (int *) malloc(10 * sizeof(int));

// do something with the memory block
// ...
// ...
// deallocate the memory block
free(ptr);
```


This code uses malloc() to allocate a block of memory for an array of ten integers and assigns the pointer to ptr. After using the memory block, it deallocates the memory block using free().


## Dynamic Memory Allocation for Arrays and Structures

In C, dynamic memory allocation can be used to allocate memory for arrays and structures. Here's an illustration:


```c
struct Person {
    char name[50];
    int age;
    float height;
};

struct Person *ptr;
ptr = (struct Person *) malloc(10 * sizeof(struct Person));
```


This code uses malloc() to allocate memory for an array of 10 Person structures and assigns the pointer to ptr.

Dynamic memory allocation in C is a powerful tool for dynamically allocating and deallocating memory during runtime. Understanding dynamic memory allocation is critical for developing programmes that can adapt to changing memory requirements and serve as a powerful data processing tool.


# Conclusion

Completing the Structured Programming in C course in its entirety can provide a strong foundation in the C programming language. Data types, control structures, functions, arrays, pointers, structures, file I/O, and dynamic memory allocation are among the topics covered in the course.

You will gain a solid understanding of the fundamentals of C programming and be able to write programmes that can perform complex tasks after completing this course. You will also gain problem-solving abilities that will be useful in a variety of fields of computer science and engineering.

While finishing the course is a significant accomplishment, it is only the beginning of your journey in learning and mastering the C programming language. Continuous practise and learning are required to improve your skills and develop your expertise. 

In conclusion, passing the Structured Programming in C course can be a significant step toward mastering C programming, opening doors to careers in software development, systems programming, and embedded systems engineering.
