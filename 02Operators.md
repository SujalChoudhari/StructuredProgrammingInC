

# C Operators

Operators are unique symbols that are used to carry out specific tasks or operations. They could be binary, unary, or occasionally ternary.

An example of an operator and a binary operator is the asterisk (*), which is used to perform multiplication in the C programming language.

All types of operators are covered in this section. 


### Arithmetic Operators

Mathematical operations like addition, subtraction, etc. are carried out using arithmetic operators. Several of the basic arithmetic operators include


<table>
  <tr>
   <td>
    Operator
   </td>
   <td>
    Description
   </td>
  </tr>
  <tr>
   <td>
    +
   </td>
   <td>
    Addition
   </td>
  </tr>
  <tr>
   <td>
    -
   </td>
   <td>
    Subtraction
   </td>
  </tr>
  <tr>
   <td>
    *
   </td>
   <td>
    Multiplication
   </td>
  </tr>
  <tr>
   <td>
    /
   </td>
   <td>
    Division
   </td>
  </tr>
  <tr>
   <td>
    %
   </td>
   <td>
    Modulus
   </td>
  </tr>
</table>



     

We must all already be familiar with their use in elementary mathematics. They serve the same function and have the same goal.  

Modulus (%) operator- this operator returns the remainder of two operands when they are divided.

 Let’s see their implementation in C.


```c
#include<stdio>
void main()
{
    int x;
    x=5%2;
    printf("remainder is %d",x);
}
```



```c
#include <stdio.h>
 
int main()
{
    int a = 2;
    int b = 3;
    printf("a + b = %d\n", a + b);
}
```


Output:


```c
a + b = 5
```


 


### Relational Operators

Relational operators are used to compare two or more numbers or even expressions in some cases. C, like Java, has six relational operators, and their return value is of the Boolean type, meaning True or False (1 or 0).

Let's look at how they're implemented in C.


```c
#include <stdio.h>
 
int main()
{
    int a = 2;
    int b = 3;
    printf("a == b = %d\n", a == b);
}
```


Output:


```c
a == b = 0
```


The output is 0, since a and b are not equal.


### Logical Operators

AND, OR, and NOT are the three logical operators. They can be used to compare Boolean values, but they are most commonly used to compare conditions to see if they are satisfying. 



* AND: it returns true when both operators are true or 1.
* OR: it returns true when either operator is true or 1.
* NOT: it is used to reverse the logical state of the operand.

<table>
  <tr>
   <td>
    Operator
   </td>
   <td>
    Description
   </td>
  </tr>
  <tr>
   <td>
    &&
   </td>
   <td>
    AND Operator
   </td>
  </tr>
  <tr>
   <td>
    ||
   </td>
   <td>
    OR Operator
   </td>
  </tr>
  <tr>
   <td>
    !
   </td>
   <td>
    NOT Operator
   </td>
  </tr>
</table>



Let’s see their implementation in C.


```c
#include <stdio.h>
 
int main()
{
    int a = 1;
    int b = 0;
    printf("a or b = %d\n", a || b);
}
```


Output:


```c
a or b = 1
```


The output is 1, since either a or b is not equal to zero.


### Bitwise Operators

A bitwise operator is used to perform operations on bits. To obtain the results, they convert our input values into binary format and then process them using the appropriate operator. 


<table>
  <tr>
   <td>
    Operator
   </td>
   <td>
    Description
   </td>
  </tr>
  <tr>
   <td>
    &
   </td>
   <td>
    Bitwise AND
   </td>
  </tr>
  <tr>
   <td>
    |
   </td>
   <td>
    Bitwise OR
   </td>
  </tr>
  <tr>
   <td>
    ^
   </td>
   <td>
    Bitwise XOR
   </td>
  </tr>
  <tr>
   <td>
    ~
   </td>
   <td>
    Bitwise Complement
   </td>
  </tr>
  <tr>
   <td>
    >>
   </td>
   <td>
    Shift Right Operator
   </td>
  </tr>
  <tr>
   <td>
    <&lt;
   </td>
   <td>
    Shift Left Operator
   </td>
  </tr>
</table>



     

Let’s see their implementation in C.


```c
#include <stdio.h>
 
int main()
{
    int a = 2; //10
    int b = 3; //11
    printf("a xor b = %d\n", a ^ b);
}
```


Output:


```c
a xor b = 1
```


The output is 1, since a xor b is 01 in binary, which is 1 in decimal.


### Assignment Operators

Assignment operators are used to assign values. We will use them in almost every program we develop.


```c
int a = 0;
int b = 1;
```


The assignment operator in this case is equal to (=). In the above example, it is assigning 0 to a and 1 to b.


<table>
  <tr>
   <td>
    Operator
   </td>
   <td>
    Description
   </td>
  </tr>
  <tr>
   <td>
    =
   </td>
   <td>
    It assigns the right-side operand value to the left-side operand.
   </td>
  </tr>
  <tr>
   <td>
    +=
   </td>
   <td>
    It adds the right operand to the left operand and assigns the result to the left operand.
   </td>
  </tr>
  <tr>
   <td>
    -=
   </td>
   <td>
    It takes the right operand and subtracts it from the left operand, then assigns the result to the left operand.
   </td>
  </tr>
  <tr>
   <td>
    *=
   </td>
   <td>
    It multiplies the right and left operands and returns the result to the left operand.
   </td>
  </tr>
  <tr>
   <td>
    /=
   </td>
   <td>
    It divides the left operand by the right operand and returns the result to the left operand.
   </td>
  </tr>
</table>



     

