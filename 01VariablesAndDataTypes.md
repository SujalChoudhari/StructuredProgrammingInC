
# C Variables

Variables are storage containers for data values. There are various types of variables in C.

An integer variable defined with the keyword int, for example, stores integers (whole numbers) without decimals, such as 91 or -13. A floating-point variable defined with the keyword float stores decimal floating-point numbers like 99.98 or -1.23.

A character variable defined with the keyword "char" stores single characters such as 'A' or 'z'. Single quotes must be used to surround char values.


### Declaration

A variable cannot be declared unless its data type is specified. A variable's data type is determined by what we want to store in it and how much space we want it to hold. The syntax for declaring variables is straightforward:


```c
data_type  variable_name;
```


OR


```c
data_type  variable_name = value;
```


 


### Naming a Variable

There are no restrictions on what we can call a variable. However, there are specific rules that must be followed when naming a variable:



* Only alphabets, digits, and underscores (_) are permitted in variable names.
* A variable must not begin with a digit.
* A variable's name cannot contain any white space.
* The name should not contain any reserved keywords or special characters. 

 

A variable can have its name changed or have its value changed, but its type cannot be changed in any way. If a variable is of the integer type, then a program can only store integer values in it. We are unable to give an integer variable a character-type value. 


#  C Data Types & Constants

As previously stated, a variable in C must be a specific data type, and the printf function must contain a format specifier in order to display the value contained in the variable. The data type describes what kind and how much data the variable will hold.


# Datatype

It refers to the kind of value that the variable stores.

Here, we'll concentrate on the most fundamental ones:


<table>
  <tr>
   <td>
    Data Type
   </td>
   <td>
    Size
   </td>
   <td>
    Description
   </td>
   <td>
    Format Specifier
   </td>
  </tr>
  <tr>
   <td>
    int
   </td>
   <td>
    2 or 4 bytes
   </td>
   <td>
    Stores whole numbers, without decimals
   </td>
   <td>
    %d or %i
   </td>
  </tr>
  <tr>
   <td>
    float
   </td>
   <td>
    4 bytes
   </td>
   <td>
    Stores fractional numbers, containing one or more decimals. Sufficient for storing 7 decimal digits
   </td>
   <td>
    %f
   </td>
  </tr>
  <tr>
   <td>
    double
   </td>
   <td>
    8 bytes
   </td>
   <td>
    Stores fractional numbers, containing one or more decimals. Sufficient for storing 15 decimal digits
   </td>
   <td>
    %lf
   </td>
  </tr>
  <tr>
   <td>
    char
   </td>
   <td>
    1 byte
   </td>
   <td>
    Stores a single character/letter/number, or ASCII values
   </td>
   <td>
    %c
   </td>
  </tr>
</table>



    Below are some sub data types


<table>
  <tr>
   <td>
    Data Type
   </td>
   <td>
    Size
   </td>
   <td>
    Description
   </td>
   <td>
    Format Specifier
   </td>
  </tr>
  <tr>
   <td>
    short int
   </td>
   <td>
    2 bytes
   </td>
   <td>
    Stores whole numbers, without decimals
   </td>
   <td>
    %sd
   </td>
  </tr>
  <tr>
   <td>
    long int
   </td>
   <td>
    4 bytes
   </td>
   <td>
    Stores fractional numbers, containing one or more decimals. Sufficient for storing 7 decimal digits
   </td>
   <td>
    %ld
   </td>
  </tr>
  <tr>
   <td>
    unsigned short int
   </td>
   <td>
    2 bytes
   </td>
   <td>
    Stores fractional numbers, containing one or more decimals. Sufficient for storing 15 decimal digits
   </td>
   <td>
    %usd
   </td>
  </tr>
  <tr>
   <td>
    unsigned long int
   </td>
   <td>
    4 bytes
   </td>
   <td>
    Stores a single character/letter/number, or ASCII values
   </td>
   <td>
    %uld
   </td>
  </tr>
</table>


 Here’s how we make use of the data type of a variable to print it:


```c
#include <stdio.h>
 int main(){
    // Creating variables of various data types
    int integer = 26;
    float floating = 39.32;
    char character = 'A';
 
    // Printing variables using their respective format specifiers, Ignore this part; we will look into it later.
    printf("%d\n", integer);
    printf("%f\n", floating);
    printf("%c\n", character);
}
```



```c
Output:
26
39.320000
A
```




# C Constants

Use the const keyword (which will declare the variable as "constant," which means unchangeable and read-only) if you don't want the variables you declare to get modified later on in your program by you or others, whether on purpose or by accident.

When a variable has values that are unlikely to change, such as any mathematical constant like PI, you should always declare it to be a constant.

A constant variable needs to have a value when it is declared.

 

This is an illustration of how to declare a constant. 


```c
#include <stdio.h>
int main()
{
    const int MOD = 10000007;
    const float PI = 3.14159265359;
}
```



# Format Specifiers & Escape Sequences

Format specifiers are codes that start with a percent sign (%), and they tell the computer how to interpret and display a certain type of data, such as a number or a string of text. For example, %d is used to display integers, %f is used to display floating point numbers, and %s is used to display strings.

Escape sequences are codes that begin with a backslash (), and they are used to represent certain special characters that cannot be typed directly into the code. For example, the escape sequence '\n' is used to represent a new line, and '\t' is used to represent a tab character.

In summary, format specifiers are used to format and display data, and escape sequences are used to represent special characters that can't be typed directly in the code.


# User Input/Output

In C, the two main functions used for input/output (I/O) operations are printf() and scanf().

printf() is used to display output to the user. The function takes one or more arguments, which are the values or expressions that you want to display. The first argument is a string that contains the text to be displayed, along with any format specifiers that indicate how the subsequent arguments should be displayed. For example, the following code will display the message "The value of x is: 5":


```
int x = 5;
printf("The value of x is: %d", x);
```


`scanf()` is used to read input from the user. The function takes two arguments: the first is a string that contains format specifiers, which indicate the type of data that the function should expect, and the second is the variable where the input will be stored. For example, the following code will prompt the user to enter an integer value and store that value in the variable x:


```
int x;
printf("Please enter an integer value: ");
scanf("%d", &x);
```


It's important to note that the & symbol is used before the variable name when passing the address of the variable to scanf(). This is because scanf() expects to receive the address of the variable in memory, where it should store the input. More information can be found in the Pointers Section.

It's also important to consider the order of input and format specifiers in scanf() function, if the order is not matched with the input, it will lead to the wrong input being stored in the wrong variable.

In conclusion, scanf() is used to read input from the user and printf() to display output to the user. Format specifiers are used by both functions to specify the kind of data that should be read or displayed.


# Storage Classes 

The visibility and lifespan of variables are managed by storage classes in the C programming language. In C, there are four storage classes: auto, register, static, and extern.



* **auto: **This is the default storage class for local variables in a function. Variables declared as auto have automatic storage duration and their visibility is limited to the block in which they are defined. When the control exits the block, the variables are destroyed.
* **register: **Variables declared as register are stored in a register instead of memory. This is used to optimize the performance of the code by reducing the access time to the variable. However, not all variables can be stored in a register and the actual storage location is implementation-dependent.
* **static:** Variables declared as static have static storage duration, meaning they are allocated at the beginning of the program and remain in memory until the end of the program. The visibility of static variables is limited to the file in which they are defined. When the program terminates, the value of static variables is lost.


### extern

The extern storage class is used to declare variables or functions defined in a different source file. The extern keyword indicates that a variable or function has external linkage, which means that it can be accessed from other source files. The declaration of an `extern `variable or function provides the compiler with information about the type and name of the entity, but does not allocate storage for it.

Here is an example of how the extern keyword can be used:


```
//File1.c
int count;

//File2.c
extern int count;
```


In this example, the variable count is defined in `File1.c`, but it can be accessed from `File2.c` by using the extern keyword. Multiple source files can now share the same variable or function.

It's important to note that `extern `variables must be defined in exactly one source file. They should be declared using the extern keyword in all other source files.

The static storage class is used to declare variables or functions that have a fixed duration of storage. This means that the variable or function is allocated at the start of the programme and remains in memory until the programme terminates.


### static

They are initialized only once, when the program starts.

Their value is retained between function calls, so they retain their value even after the function in which they are defined returns.

They have internal linkage, meaning they can only be accessed within the source file in which they are defined.

Here is an example of how the static keyword can be used to declare a static variable:


```
#include <stdio.h>

void printCount() {
  static int count = 0;
  count++;
  printf("count: %d\n", count);
}

int main() {
  printCount(); // Outputs: count: 1
  printCount(); // Outputs: count: 2
  printCount(); // Outputs: count: 3
  return 0;
}
```


Inside the printCount function, the variable count is declared as static. When the function is called for the first time, count is set to 0. The value of count is retained between function calls, so the value of count is incremented by one each time the function is called. This enables the function to retain its state across multiple calls.


### auto

`auto `is the default storage class for local variables in a function. Variables declared as auto have an automatic storage duration, which means they are created when the function is called and destroyed when it returns. Auto variables are only visible in the block in which they are defined.


### register

Variables declared as `register `are stored in a register instead of memory. This can be used to improve code performance by shortening the access time to the variable. However, not all variables can be stored in a register, and the actual storage location varies depending on the implementation.


# Type Casting

In C, type casting is a method of converting one data type to another. It entails assigning a new data type to a value or expression. This can be useful when converting a value from one type to another to perform operations or when storing a value of one type in a variable of another type.

C supports two types of type casting:



* **Implicit type casting:** This is performed automatically by the compiler and occurs when a value of one type is converted into a value of another type. For example, when an int is assigned to a float variable, implicit type casting takes place.
* **Explicit type casting:** This is performed manually by the programmer and involves explicitly specifying the desired type. This is done using type casting operators, such as (type), where type is the desired data type.


### Implicit type casting

Implicit type casting, also known as type promotion or type coercion, is a type of type casting that the compiler performs automatically. It happens when a value of one type is implicitly converted into a value of another type, usually one with a wider range or greater precision.

Implicit type casting in C adheres to a set of type promotion rules. Based on the types in an expression, the rules determine which data type a value will be implicitly converted to. The following are the most common types of promotions:



* When an `int` is added to a `float`, the `int` is promoted to a `float`.
* When a `short` is added to an `int`, the `short` is promoted to an `int`.
* When a `char` is added to an `int`, the `char` is promoted to an `int`.

Here is an example of implicit type casting:


```
int a = 10;
float b = 3.14;
float result = a + b;  // implicit type casting of int to float
```


The value of a in this example is an int, and the value of b is a float. When a and b are added, the int value of a is implicitly converted to a float to match the type of b. The result of the addition is stored in the float variable result.

Implicit type casting can cause unexpected behaviour, such as loss of precision, so it's best to be aware of the type promotion rules and explicitly cast values as needed.


### Explicit Type Conversion

Explicit type casting is a type of type casting that is performed explicitly by the programmer. It is also known as type casting or type conversion. It entails specifying the desired data type for a value or expression explicitly. 

Explicit type casting in C is accomplished with the type casting operator (type), where type is the desired data type. As an example:


```
float x = 3.14;
int y = (int) x;  // explicit type casting of float to int
```


The value of the float variable x is explicitly cast to an int using the type casting operator in this example, and the result is stored in the int variable y. It should be noted that explicit type casting can result in precision loss, so it should be used with caution.

Here's another illustration:


```
int a = 10;
float b = 3.14;
float result = (float) a + b;  // explicit type casting of int to float
```


The value of a is explicitly cast to a float using the type casting operator in this example, and the result of the addition is saved in the float variable result.


# Enumerated data types

An enumerated data type, also known as an enum, is a C user-defined data type that represents a collection of named constants. The enum keyword is used to declare an enum type, which is then followed by the enumerated constants in curly braces. As an example:


```
enum days {Mon, Tue, Wed, Thu, Fri, Sat, Sun};
```


In this example, an enumerated data type days is declared with seven constants: Mon, Tue, Wed, Thu, Fri, Sat, and Sun. By default, the first constant is assigned the value 0, and each subsequent constant is assigned the value of the previous constant plus 1. For example, Mon is assigned the value 0, Tue is assigned the value 1, and so on.

You can also explicitly assign values to the constants in an enum:


```
enum days {Mon=1, Tue, Wed, Thu, Fri, Sat, Sun=7};
```


In this example, Mon is assigned the value 1, and Sun is assigned the value 7. The values for the remaining constants are assigned automatically, so Tue is assigned the value 2, Wed is assigned the value 3, and so on.

Once an enum is declared, you can use the constants in your code just like you would use any other constant. For example:


```
days today = Mon;

if (today == Mon) {
    printf("Today is Monday\n");
}
```


Enumerated data types are useful when you need to define a set of named constants that represent a specific set of values, such as days of the week or directions. They can make your code more readable and easier to maintain, as named constants are easier to understand than raw numeric values.

Hence,


```
int Mon = 1;
int Tue = 2;
...
// can be replaced by
enum days {Mon,Tue,...};
```

