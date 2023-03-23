
# Strings

Let's start with strings. A "string" in computer programming is a sequence of characters, such as letters, numbers, punctuation, and symbols, used to represent text. Strings are commonly used to store names, sentences, and other types of text data. In C, strings are represented as arrays of characters, where the last character in the array is the null character `'\0'`. For example, the string "Hello" can be represented as a character array like this:


```c
char greeting[6] = {'H', 'e', 'l', 'l', 'o', '\0'};
```


Strings can also be declared and initialised using string literals, which are sequences of characters surrounded by double quotes:


```c
char greeting[] = "Hello";
```


In this example, the size of the character array is automatically determined based on the number of characters in the string literal.

To manipulate strings in C, various string functions are provided in the `string.h` library. Some commonly used string functions are `strlen`, which returns the length of a string, `strcpy`, which copies one string to another, `strcat`, which concatenates two strings and `strcmp`, which compares two strings.

_The string.h header file is not required to use the strlen function because it is part of the standard C library and is included by default in most C compilers. However, including the string.h header file adds a declaration for strlen and other string functions, making it easier for the compiler to check their usage and avoiding potential errors._

_When using library functions, it's generally a good idea to include the relevant header file, even if it's not strictly necessary. This makes the code more readable and portable by making it clear which functions are being used and which library is being used._

_While the strlen function can be used without including string.h, it is generally thought to be a good idea to do so. _

Here's an example of using the `strlen `function to find the length of a string:


```c
#include <stdio.h>
#include <string.h>

int main() {
    char name[] = "John Doe";
    int length;

    length = strlen(name);
    printf("The length of the string is: %d\n", length);

    return 0;
}
```


Let's look at other String Functions


## String Functions

We can use C's string handling library functions to handle strings. The string.h library is used to perform string operations. It provides several functions for manipulating strings. 

Following are some commonly used string handling functions:


### strcat()

This function is used to concatenate the source string to the end of the target string. This function expects two parameters, first, the base address of the source string and then the base address of the target string. For example, “Hello” and “World” on concatenation would result in a string “HelloWorld”. 

Here is how we can use the strcat( ) function:


```c
#include <stdio.h>
#include <string.h>
int main()
{
    char s[] = "Hello";
    char t[] = "World";
    strcat(s, t);
    printf("String = %s", s);
}
```


Output:


```c
String  = HelloWorld
```



### strlen()

This function is used to count the number of characters present in a string.

Here is how we can use the strlen( ) function:


```c
#include <stdio.h>
#include <string.h>
int main()
{
    char s[] = "Hello";
    int len = strlen(s);
    printf("Length = %d", len);
}
```


Output:


```c
Length  = 5
```



### strcpy()

This function is used to copy the contents of one string into the other. This function expects two parameters, first, the base address of the source string and then the base address of the target string.

Here is how we can use the strcpy( ) function:


```c
#include <stdio.h>
#include <string.h>
int main()
{
    char s[] = "C is Good";
    char t[50];
    strcpy(t, s);
    printf("Source string = %s\n", s);
    printf("Target string = %s", t);
}
```


Output:


```c
Source string  = C is Good
Target string  = C is Good
```



### strcmp()

The strcmp() function is used to compare two strings to find out whether they are the same or different. It takes two strings as two of its parameter. It will compare two strings, character by character until there is a mismatch or the iterator reaches the end of one of the strings.

If both of the strings are identical, strcmp( ) returns a value of zero. If they are not identical, it will return a value less than zero, considering the ASCII value of the mismatched character in the first string is less than the mismatched character in the second string. Else, it will return a value greater than 0.

Here is how we can use the strcmp( ) function:


```c
#include <stdio.h>
#include <string.h>
int main()
{
    char s[] = "Hello";
    char t[] = "World";
    int cmp = strcmp(s, t);
    printf("Comparison result = %d", cmp);
}
```


Output:


```c
Comparison result = -1
```



### strrev()

This function is used to return the reverse of the string. 

Here is how we can use the strrev( ) function:


```c
#include <stdio.h>
#include <string.h>
int main()
{
    char s[] = "Hello";
    printf("Reversed string = %s", strrev(s));
}
```


Output:


```c
Reversed string  = olleH
 
```


