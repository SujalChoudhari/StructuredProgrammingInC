
# Conditional Statements


## If - Else


    When we want to execute one set of instructions if a certain condition is met and another set of instructions if it is not, we use conditional logic. In C, a decision control system is used to handle situations like this. 


    The if statement's condition is always enclosed by a pair of parentheses. If the condition is met, the set of statements following the if statement will be carried out. If the condition evaluates to false, the statement will not be executed; instead, the program will skip the enclosed section of code.


    Relational operators are used to define expressions in if statements. When we compare two values using relational operators, we can determine whether they are equal, unequal, greater than, or less than.


    If we want to execute a specific code in one situation and another, opposite, or different code if that situation does not occur, we can use if statements. It all depends on the situation. If the condition returns true, the situation has occurred, and the true part of the code will be executed; otherwise, the false part of the code will be executed.


     


<table>
  <tr>
   <td>
    Conditions
   </td>
   <td>
    Meaning
   </td>
  </tr>
  <tr>
   <td>
    a == b
   </td>
   <td>
    a is equal to b
   </td>
  </tr>
  <tr>
   <td>
    a != b
   </td>
   <td>
    a does not equal b abb.
   </td>
  </tr>
  <tr>
   <td>
    a &lt; b
   </td>
   <td>
    a is less than b
   </td>
  </tr>
  <tr>
   <td>
    a > b
   </td>
   <td>
    a is greater than b
   </td>
  </tr>
  <tr>
   <td>
    a &lt;= b
   </td>
   <td>
    a is less than or equal to b
   </td>
  </tr>
  <tr>
   <td>
    a >= b
   </td>
   <td>
    a is greater than or equal to b
   </td>
  </tr>
</table>



     


    When the expression following if evaluates to true, the statement in an if block is executed. However, if the if block is followed by an else block, the set of statements in the else block will execute if the condition written in the if block is false.


    The syntax for if-else statements is as follows:


```
if ( condition ){
    statements;
}else {
    statements;
}
```


For example, in the given code, it checks if the number is less than or equal to 10, and if it is true, it will print "Number is less than or equal to 10." If it's false, it will print "Number is greater than 10."


```
#include <stdio.h>
 
int main()
{
    int num = 10;
    if (num <= 10)
    {
        printf("The number is less than or equal to 10.");
    }
    else
    {
        printf("Number is greater than 10.");
    }
    return 0;
}
```


 Output


```
The number is less than or equal to 10.
```



## If-Else Ladder

We can also use ladder if-else to test multiple conditions. If the previous condition is false, it only checks the next condition.


```
if(/*conditon*/)
{
    //statements
}
else if(/*condition*/)
{
    //statements
}
else if(/*condition*/)
{
    //statements
}
else {
    //statements
}
```


This code is an example of using the if-else statement to check multiple conditions. The if statement is used to check the first condition. If the first condition is true, the code inside the first set of curly braces ({}) will be executed. If the first condition is false, the else if statement will be used to check the second condition. If the second condition is true, the code inside the second set of curly braces will be executed. If the second condition is false, the else if statement will be used to check the third condition. If the third condition is true, the code inside the third set of curly braces will be executed. If all conditions are false, the code inside the final else statement will be executed.

In this code, the conditions inside the if, else if statements are left blank, you need to put the conditions you want to check in that place.

It's important to note that the code inside the else block will only be executed when all the conditions above it are false.


## Nested if-else

An entire if-else statement can also be written within the body of another if statement or the body of an else statement. This is known as the "nesting" of ifs.


```
if(/*condition*/) {
	if(/*condition2*/) {
		//statement
	}
	else {
		//statement 
	}
}
else
{
//statements
}
```


This code is an example of using nested if-else statements. The outer if statement is used to check the first condition. If the first condition is true, the code inside the first set of curly braces ({}) will be executed. Inside the first set of curly braces, there is another if-else statement, this is the inner if-else statement. The inner if statement is used to check the second condition. If the second condition is true, the code inside the second set of curly braces will be executed. If the second condition is false, the code inside the else block of the inner if-else statement will be executed. If the first condition is false, the code inside the else block of the outer if-else statement will be executed.

It's important to note that the inner if-else statement is only executed when the outer if statement's condition is true. The inner if-else statement is nested within the outer if-else statement.

In this code, the conditions inside the if, else if statements are left blank, you need to put the conditions you want to check in that place.


# Switch Case Statements

A switch statement is a control flow statement that allows you to test a variable or expression against multiple possible cases, or "branches". The basic syntax of a switch statement looks like this:


```
switch (expression) {
    case value1:
        // code to be executed if expression == value1
        break;
    case value2:
        // code to be executed if expression == value2
        break;
    case value3:
        // code to be executed if expression == value3
        break;
    ...
    default:
        // code to be executed if expression does not match any of the cases
}
```


In the above example, the variable or expression that is being tested is evaluated once, and then the corresponding block of code is executed for the first matching case. The break statement is used to exit the switch statement and continue with the code that follows it. If the expression does not match any of the cases, the code in the default case will be executed.

The main difference between an if-else statement and a switch statement is the way that the conditions are evaluated. In an if-else statement, each condition is evaluated one by one until a true condition is found, at which point the corresponding block of code is executed. In a switch statement, the expression is evaluated once, and then the corresponding block of code is executed for the first matching case.

A switch statement is generally more efficient than a series of if-else statements when you have a large number of cases to test. It can also make your code more readable and easier to understand if you have a lot of conditions to test.

It's important to note that switch statements can only be used with integers, characters, and some enumerated types. And also, the case values should be unique and constant.


### Rules for Switch statements



* Switch's test expression must always be an int or char.
* The case value should be an integer or a character.
* Cases should be used only within the switch statement.
* The break keyword is not required in the switch statement.
* The case label values within the switch should be distinct. 

The break keyword does not have to be used after every case. Break keywords should be used only when we want to end our case at that point; otherwise, we won't. We can also use nested switch statements, which are switches inside switches. Furthermore, the case constants of the inner and outer switches can have the same value without causing any conflicts.


# Break, Continue and Goto

In C programming, there are certain statements that can change the flow of control in a program:


## Break Statement:

This statement is used to exit a loop or a switch statement. When the program reaches a break statement inside a loop or a switch, it will exit the loop or switch and continue with the next line of code after the loop or switch.





## Continue Statement:

The continue statement is used to skip the current iteration of a loop and proceed to the next iteration. When a continue statement is encountered within a loop, the program skips the remaining code in that iteration and moves on to the next.





## Goto statement: 

This statement passes control to a labeled statement. It enables you to navigate to a specific point in the code. The labeled statement is distinguished by a distinct label followed by a colon.

It's important to note that using the "goto" statement in a program is generally not recommended because it can make the program difficult to understand and debug.





# Loops

In programming, we frequently have to repeat the same action with little or no variation in the details each time it is executed. This requirement is met by a mechanism known as a "loop."

The computer's versatility stems from its ability to repeatedly execute a set of instructions. This involves repeating some code in the program a specified number of times or until a specific condition is met. Loop-controlled instructions are used to perform this repetitive operation efficiently, ensuring that the program does not appear redundant due to the repetitions.

The three types of loops in C programming are as follows.



* For loop
* While loop
* do-while loop

 


## Types of Loops


### Entry Controlled Loops

In entry-controlled loops, the test condition is evaluated before entering the loop body. Entry-controlled loops include the for loop and the while loop.


### Exit Controlled Loops

The test condition is tested at the end of the loop in exit-controlled loops. The loop body will execute at least once regardless of whether the test condition is true or false. An example of an exit-controlled loop is the do-while loop.

 


## For Loop

A for loop is a repetition control structure that allows us to write a loop that will execute a specific number of times in an efficient manner. The for loop operates as follows:

The initialization statement is only executed once; in this statement, we set a variable to a value.

The test expression is evaluated in the second step. Assume the test expression is found to be true. The for loop continues to run and the test expression is re-evaluated in that case, but if the test expression is evaluated to false, the for loop terminates.

The loop continues to execute until the test expression is false. The loop is terminated when the test expression is false. 


```
// for loop
for (int i = 0; i < 10; i++) {
    printf("%d ", i);
}
```


The for loop is used when the number of iterations is known in advance. The for loop has three parts: the initializer, the condition, and the increment/decrement. The initializer is executed only once, before the loop starts. The condition is evaluated before each iteration, and if it is true, the loop continues. The increment/decrement is executed after each iteration.

 


## While loop

A while loop is also known as a pre-tested loop.  The while loop allows code to be run multiple times based on a boolean condition specified as a test expression. While introducing for loops, we saw that the number of iterations is known, whereas while loops are used when the number of iterations of the loop is unknown.  The while loop is terminated based on the test condition, which is either true or false.


```
// while loop
int i = 0;
while (i < 10) {
    printf("%d ", i);
    i++;
}
```


The while loop is used when the number of iterations is not known in advance, or when you want the loop to continue until a certain condition is met. The while loop has one part: the condition. The condition is evaluated before each iteration, and if it is true, the loop continues.


### Properties of the while loop:

Following are some of the properties of the while loop.



* A conditional expression written in the brackets of while is used to check the condition. The Set of statements defined inside the while loop will execute until the given condition returns false.
* The condition will return 0 if it is true. The condition will be false if it returns any nonzero number.
* In the while loop, we cannot execute the loop until we do not specify the condition expression.
* It is possible to execute a while loop without any statements. This will give no error.
* We can have multiple conditional expressions in a while loop.
* Braces are optional if the loop body contains only one statement.


## Do-While loop

In do-while loops, the execution is terminated based on the test condition, just like in a while loop. The main difference between the do-while loop and the while loop is that the condition is tested at the end of the loop body in the do-while loop, whereas the other two loops are entry-controlled. Regardless of the test condition, the loop body will execute at least once in a do-while loop.


```
// do-while loop
int i = 0;
do {
    printf("%d ", i);
    i++;
} while (i < 10);
```


The do-while loop is similar to the while loop, but it guarantees that the loop will be executed at least once, because the condition is evaluated after the first iteration.

In the above examples, all three loops will run 10 times and print the values of i from 0 to 9.

It is sometimes necessary to exit a loop while it is being executed. We use the break and continue statements to accomplish this.


### Difference between a while and a do-while loop

A while loop is executed every time the given test condition returns true, whereas, a do-while loop is executed for the first time regardless of whether the test condition is true or false because the test condition is checked only after executing the loop for the first time.


### Using Continue and Break in Loops

Here's an example of using the continue statement in a for loop:


```
for (int i = 0; i < 10; i++) {
    if (i % 2 == 0) {   // if i is even
        continue;      // skip the remaining code in this iteration and move on to the next iteration
    }
    printf("%d ", i);  // this code will only be executed if i is odd
}
```


In this example, the for loop iterates 10 times, but the printf statement inside the loop only gets executed for the odd values of i because the even values of i are skipped using the continue statement. The output of this code will be:


```
1 3 5 7 9 
```


Here's an example of using the break statement in a while loop:


```
int i = 0;
while (i < 10) {
    if (i == 5) {      // if i is 5
        break;        // exit the while loop
    }
    printf("%d ", i);  // this code will be executed until i is 5
    i++;
}
```


In this example, the while loop iterates until the value of i becomes 5, but the printf statement inside the loop only gets executed until the value of i becomes 5 because of the break statement. The output of this code will be:


```
0 1 2 3 4 
```


As you can see, the break statement terminates the loop whenever the condition inside the if statement becomes true. while the continue statement skips the current iteration and continues with the next iteration.

