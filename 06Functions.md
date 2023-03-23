

# Functions

A function is a piece of code that accomplishes a specific task and may return a value. Code is structured and modularized using functions, making it easier to understand, maintain, and reuse.

 A function describes how to perform a specific task in a programme, much like a recipe describes how to prepare a dish.

A recipe in a cookbook has a name, such as "chocolate cake," that describes what the recipe does. A recipe also includes a list of ingredients as well as instructions on how to combine the ingredients and bake the cake.

A function, like "add" or "calculateAverage," has a name that describes what the function does. A function also has a list of parameters that serve as ingredients, as well as a set of instructions that perform a specific task, such as adding two numbers or calculating the average of a set of numbers.

You can reuse a function in a programme as many times as you need, just like you can reuse a recipe in a cookbook. This improves code organisation, reusability, and maintainability.

A function in C is defined with the following syntax:


```c
return_type function_name(parameter_list) {
    // function body
}
```




* **return_type** is the data type of the value that the function returns. If the function does not return a value, void is used as the return_type.
* **function_name** is the name of the function. It should be a descriptive name that reflects what the function does.
* **parameter_list** is a list of parameters that the function takes as input. It can be empty, or it can contain one or more parameters separated by commas. Each parameter is defined with its data type and name.

Here's an example of a function that takes two integers as parameters and returns their sum:


```c
int add(int a, int b) {
    int result = a + b;
    return result;
}
```


To call a function, simply use its name followed by its arguments in parentheses:


```c
int x = 5, y = 3;
int sum = add(x, y);
printf("The sum of %d and %d is %d\n", x, y, sum);
```


This outputs:


```c
The sum of 5 and 3 is 8
```


In this example, the add function is called with the arguments x and y, and the result is stored in the variable sum. The printf function is then used to display the result.

Functions can be called as many times as needed, making it easier to reuse code. Functions can also call other functions, allowing for further modularization and abstraction. This makes code more maintainable and helps to avoid duplication of code.


## Function Declaration

A function declaration is a prototype of a function that specifies the function's name, return type, and the types and number of arguments that it takes. It is typically placed in a header file so that it can be used by other parts of the programme. A function declaration has the following syntax:


```c
return_type function_name(arg1_type arg1, arg2_type arg2, ...);
```


For Example,


```c
int add(int a, int b);
```



## Function Definition

A function definition is the actual implementation of a function that specifies the code that the function executes. The function definition must match the function declaration in terms of the function's name, return type, and the types and number of arguments that the function takes. The function definition has the following syntax:


```c
return_type function_name(arg1_type arg1, arg2_type arg2, ...) {
   // function code
}
```


Example


```c
int add(int a, int b) {
   return a + b;
}
```



## Function Call

A function call is an expression that invokes a function and passes arguments to it. The function call has the following syntax:


```c
function_name(arg1, arg2, ...);
```


For example:


```c
int x = 10, y = 20;
int sum = add(x, y);  // function call
```


In this example, the add function is called with the arguments x and y, and the result of the function is stored in the variable sum.

An Argument can be passed in two ways: by value and by reference. These are Pass by reference examples. Pointers will cover these topics.


## Not-parameterized Functions

A normal function, also known as a non-parameterized function, is a function that does not take any input parameters. It performs a specific task and can return a value, but does not require any input from the calling code. An example of a normal function is the printf function, which outputs text to the console.


```c
#include <stdio.h>

void printMessage() {
    printf("Hello, world!\n");
}

int main() {
    printMessage();
    return 0;
}
```



## Parameterized Functions

A parameterized function, on the other hand, takes input parameters and performs its task based on those inputs. The parameters are defined in the function signature, and their values are passed to the function when it's called. An example of a parameterized function is the add function, which adds two numbers:


```c
#include <stdio.h>

int add(int a, int b) {
    int result = a + b;
    return result;
}

int main() {
    int x = 5, y = 3;
    int sum = add(x, y);
    printf("The sum of %d and %d is %d\n", x, y, sum);
    return 0;
}
```


In this example, the add function takes two input parameters, a and b, and returns the sum of these numbers. When the function is called with the arguments x and y, it performs the addition and returns the result, which is then stored in the variable sum.

Using parameterized functions makes code more flexible and reusable, as the same function can be used with different input values to perform the same task.


## Correct way of declaring, defining and calling a function


```c
#include <stdio.h>

// Function prototype declaration
int add(int a, int b);

int main() {
    int x = 5, y = 3;
    int sum;

    // Function call
    sum = add(x, y);

    printf("The sum of %d and %d is %d\n", x, y, sum);
    return 0;
}

// Function definition
int add(int a, int b) {
    int result = a + b;
    return result;
}
```


In this example:

The function declaration int add(int a, int b); tells the compiler about the function's name, return type, and parameter list. This declaration is usually placed at the top of the program, before the main function.

The function definition int add(int a, int b) provides the implementation of the function. It contains the statements that define what the function does. The function definition starts with the function signature, which must match the declaration, and includes the return type, the function name, and the parameter list.

The function call sum = add(x, y); invokes the function and passes the values of x and y as arguments. The function performs its task and returns a value, which is stored in the sum variable.

In general, the correct way to declare, define, and call a function in C is:



* Declare the function before the main function, providing the function signature and return type.
* Define the function after the main function, providing the implementation and return statement.
* Call the function in the main function, passing any required arguments, and assign the returned value to a variable if needed.

It's important to ensure that the function declaration and definition match, including the return type, function name, and parameter list. The compiler uses the declaration to check the syntax of the function call and the definition to generate the code that implements the function's behaviour.


## Using Functions without Prototype Declaration

In C, it is possible to call a function without declaring its prototype first, as long as the function definition appears before its first use in the code. This means that the function definition acts as both the declaration and the definition.

Here is an example of how to define and call a function without declaring its prototype:


```c
#include <stdio.h>

int add(int a, int b) {
    int result = a + b;
    return result;
}

int main() {
    int x = 5, y = 3;
    int sum;

    sum = add(x, y);

    printf("The sum of %d and %d is %d\n", x, y, sum);
    return 0;
}
```


In this example, the function add is defined before its first use, so there is no need to declare its prototype. The function can be called from the main function, and its behavior is determined by the definition.

However, it's good practice to always declare the prototypes of all functions used in a program, as it makes the code more readable and helps to catch any syntax errors early on in the development process.


## Recursion

Recursion is a programming technique where a function calls itself in order to solve a problem. In other words, a recursive function is a function that repeats itself until a certain condition is met. The condition is usually expressed in terms of a base case, which is a simple case that can be solved without recursion. All other cases are expressed in terms of recursive calls to the same function.

Here's an example of a recursive function in C that calculates the factorial of a number:


```c
#include <stdio.h>

int factorial(int n) {
    if (n == 0) {
        return 1;
    }
    else {
        return n * factorial(n - 1);
    }
}

int main() {
    int num = 5;
    int result;

    result = factorial(num);

    printf("The factorial of %d is %d\n", num, result);

    return 0;
}
```


In this example, the function factorial calculates the factorial of a number by repeatedly calling itself with a reduced value of the argument until the base case n == 0 is reached. The base case returns the value 1, which is then multiplied by the intermediate results obtained from the recursive calls. The final result is returned to the original call and printed by the main function.

Recursion can be a powerful tool for solving complex problems, but it can also lead to infinite loops if the base case is not specified correctly. It's important to choose the right problem and to carefully design the recursive function to ensure that it terminates correctly.


## Similarity and Differences between Recursive Functions and Loops


### Similarities



* Both can be used to repeat a task a specified number of times or until a certain condition is met.
* Both can be used to solve problems that involve repetitive calculations or operations.


### Differences



* Loops use iteration to repeat a task, while recursion uses function calls to repeat the task.
* Loops have an explicit counter or control variable, while recursion has a set of recursive calls that form a chain of function calls.
* Loops can be implemented using for, while, and do-while constructs, while recursion requires a function to call itself.
* Loops are generally faster and use less memory than recursion, but they can lead to code that is harder to understand and maintain. Recursion, on the other hand, can lead to elegant and readable code, but it can also lead to stack overflow errors if the recursion depth is too great.

In general, the choice between recursion and loops depends on the specific problem being solved and the preferred style of the programmer. Both techniques have their strengths and weaknesses, and both can be used effectively in different situations. It's important to choose the right technique for the task at hand and to understand the trade-offs involved in each approach.
