
# Arrays

An array is a collection of elements of the same data type stored in contiguous memory locations. Arrays can be used to store multiple values in a single variable, instead of declaring separate variables for each value. The elements in an array are accessed by their index, which starts from 0. The syntax for declaring an array in C is as follows:


```c
data_type array_name[array_size];
```


For example, to declare an array of 5 integers, you would use:


```c
int numbers[5];
```


You can also initialize an array at the time of declaration:


```c
int numbers[5] = {1, 2, 3, 4, 5};
```


You can access the elements of an array using the array name and the index of the element within square brackets:


```c
numbers[0] = 10;
printf("%d\n", n);
```


Arrays can be passed to functions as arguments and returned from functions. The size of an array can be obtained using the sizeof operator.

The length of an array is the number of elements it contains and can be obtained using `sizeof(array_name) / sizeof(data_type).`

A multi-dimensional array is an array of arrays. It is a data structure that allows you to store multiple arrays of data in a single array.

The syntax for declaring a two-dimensional array is as follows:


```c
data_type array_name[rows][columns];
```


For example, the following declares a two-dimensional integer array named matrix with 3 rows and 4 columns:


```c
int matrix[3][4];
```


You can also initialize a two-dimensional array at the time of declaration:


```c
int matrix[3][4] = {
   {1, 2, 3, 4},
   {5, 6, 7, 8},
   {9, 10, 11, 12}
};
```


In a similar manner, you can declare and initialize arrays with more than two dimensions. Accessing elements in a multidimensional array requires multiple indices. For example, to access the element at row 2 and column 3 in the above matrix array, you would use `matrix[1][2]`.


## Operations on Array

We learned what an array is in the last section, which served as an introduction. Now we'll take a closer look at some of the things arrays can do. 

The user can declare arrays by specifying the data type, followed by the array name and the array size in square brackets. As an example:


```c
int myArray[10];
```


This creates an integer array with 10 elements, where each element can be accessed by its index number, starting from 0. For example, to access the first element of the array, you would use `myArray[0]`, the second element would be `myArray[1]` and so on.

It is important to note that the array size must be a constant value because the compiler uses it to allocate memory for the array. Also, once an array is declared, its size cannot be changed.


## Taking data from User

To populate an array with values inputted by the user, you can use a loop along with the `scanf()` function. The `scanf()` function allows the user to input values that are stored in a specified variable.

Here's an example of populating an array of size 10 with integer values inputted by the user:


```c
#include <stdio.h>

int main() {
    int myArray[10];
    int i;

    for (i = 0; i < 10; i++) {
        printf("\nEnter an integer: ");
        scanf("%d", &myArray[i]);
    }

    return 0;
}
```



## Matrix Representation in an Array (2D)

A matrix is a 2D array where each element can be thought of as a row and column intersection. Here's an example of declaring and initialising a 2x2 matrix in C:


```c
#include <stdio.h>

int main() {
    int matrix[2][2] = { {1, 2}, {3, 4} };
    int i, j;

    printf("The matrix is:\n");
    for (i = 0; i < 2; i++) {
        for (j = 0; j < 2; j++) {
            printf("%d ", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```


This outputs:


```c
The matrix is:
1 2
3 4
```


Operations that can be performed on matrices include matrix addition, matrix subtraction, matrix multiplication, and finding the transpose of a matrix.

Matrix addition and subtraction are done element by element, that is, by adding or subtracting corresponding elements from two matrices. For example, the addition of two matrices A and B of the same size results in a matrix C, where each element `c[i][j]` is the sum of elements` a[i][j]` and `b[i][j]`.

Matrix multiplication is accomplished by multiplying the elements of one matrix's row by the elements of another matrix's column and then adding the results. The dimensions of the resulting matrix are equal to the number of rows in the first matrix and the number of columns in the second matrix.

To find the transpose of a matrix, swap its rows and columns, so that the i-th row becomes the i-th column and vice versa. 

Here's an example of finding the transpose of a 2x3 matrix in C:


```c
#include <stdio.h>

int main() {
    int original[2][3] = { {1, 2, 3}, {4, 5, 6} };
    int transposed[3][2];
    int i, j;

    printf("The original matrix is:\n");
    for (i = 0; i < 2; i++) {
        for (j = 0; j < 3; j++) {
            printf("%d ", original[i][j]);
        }
        printf("\n");
    }

    for (i = 0; i < 2; i++) {
        for (j = 0; j < 3; j++) {
            transposed[j][i] = original[i][j];
        }
    }

    printf("The transposed matrix is:\n");
    for (i = 0; i < 3; i++) {
        for (j = 0; j < 2; j++) {
            printf("%d ", transposed[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```


This outputs:


```c
The original matrix is:
1 2 3
4 5 6
The transposed matrix is:
1 4
2 5
3 6
```


The original matrix is shown first, followed by the transposed matrix, which is found by swapping the rows and columns using nested loops. The transposed matrix that results is then displayed. That's all there is to arrays; you'll learn more about them as you use them. 
