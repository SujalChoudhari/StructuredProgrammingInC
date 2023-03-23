# Why should we learn C/ Features of C?

* As referenced above, it is one of the most famous programming languages on the planet.
* Learning some other famous programming language, for example, Python or C++, turns into a cakewalk now  that you know C.
* C is an adaptable language and that gets demonstrated by the way that it tends to be utilized in different applications as well as advancements.
* C is fast when compared with other programming language like Java or Python.
    * Because source code of C is directly compiled down to Machine Code.
    * When it comes to speed, C sets up the standards. A great deal of Python libraries, for example, NumPy, Pandas, Scikit-learn, and so on are fabricated utilizing C.
* Being near Machine language, a portion of its capabilities incorporate direct admittance to machine-level equipment APIs.
* It is procedural programming language (POP) Procedural Writing computer programs is the utilization of code in a stage wise methodology to foster applications.
    * C focuses on how the data is processed rather than how the data is stored/accessed.


# Getting everything rolling with C

To begin utilizing C, you want two things:

a text editor, similar to Notebook, or an IDE, such as VS Code, to go about as a stage for you to write C code. a compiler, such as GCC, to compile the C code you have written, which is a higher-level language, into a low-level language that the PC will comprehend.


# What is an IDE?

IDE represents an **Integrated Development Environment**.

It is simply an improved version of a text editor tool that assists you in writing more effective and pleasant code.

It has a number of features, including IntelliSense, which can predict where errors may occur even before the code is compiled. Appropriate warnings are issued, along with suggestions for correction. All debugging tools are included to make coding more enjoyable.

There are numerous IDEs available, including DEV C++ or Code Blocks, Visual Studio, and VSCode. Most colleges use the Turbo C IDE, which, while old, is a good place to start because it is simple to set up and has a functional help menu.


# Compilation Process

Understanding the compilation process is much more important than memorizing syntax. As a developer, you need to know how your tools work so that you can squeeze more from them. You should have an idea of what happens to your written source code.


Source code is passed through various processes.

1. Preprocessor
2. Compiler
3. Assembler
4. Linker
5. Loader/Runner

### Preprocessor

Preprocessors are applications that modify our source code before compilation, as the name suggests. When writing a program in C or C++, there are several steps between writing the program and running it. 

A preprocessor is just a more sophisticated version of the find and replace tool. Under the hood, the preprocessor opens the stdio.h file, copies its contents, and pastes them in the spot where you specify `#include &lt;stdio.h>`. This applies to macros and file inclusion.

There are four main types of preprocessor directives:  



* Macros
* File Inclusion
* Conditional Compilation
* Other directives

In upcoming tutorials on advanced C, we'll investigate it. For the time being, keep in mind that preprocessing happens before compilation.

### Compiler

The C compiler software is used during the compilation phase to convert the intermediate (.i) file into an assembly file (.s) containing assembly level instructions (low-level code). The compiler converts the intermediate file into an assembly file to improve program performance.

Assembly code is a simple English-like language used to write low-level instructions (assembly language is used in microcontroller programs). The compiler software parses (syntax analyzes) the entire program code in one pass and reports any syntax errors or warnings in the source code via the terminal window.

The image below depicts how the compilation phase works.



### Assembling

An assembler is used to convert assembly level code (.s files) into machine-readable code (in binary/hexadecimal form). An assembler is a pre-written program that converts assembly code to machine code. It takes basic instructions from an assembly code file and converts them into machine-specific binary/hexadecimal code known as object code.

The generated file has the same name as the assembly file and is an object file with the extension ".obj" in DOS and ".o" in UNIX OS. 

The image below depicts how the assembly phase works. The name of an assembly file area.s is translated to the name of an object file area.o with a different extension.



### Linking

Linking refers to the process of incorporating library files into our program. Library files are predefined files that contain the definition of functions in machine language and have the extension ".lib." The object (.o/.obj) file contains some unknown statements that our operating system does not understand. You can think of this as a book with some unfamiliar words in it, and you'll use a dictionary to figure out what they mean. Similarly, we use libraries to provide context for some undefined statements in our object file. The linking process results in the creation of an executable file with the extension ".exe" in DOS and “.out” in UNIX OS.

The image below shows how the linking phase works. We have an object file with machine-level code, and it is passed through the linker, which links the library files with the object file to generate an executable file.



# Basic Structure and Syntax

Programming in C involves following a basic structure throughout. Here’s what it can be broken down to:



* Preprocessor commands
* Functions
* Variables
* Statements
* Expressions
* Comments


## Preprocessor commands

When our source code is compiled, Preprocessor is the first candidate to get the code. Some parts of the code are evaluated even before compiling. This adds functionality to a program.

Here is an example.


```c
#include <math.h>
```


We incorporate math.h to have the option to utilize a few unique capabilities, like power and absolute.` #include<your_file_name.h>` is the way by which we incorporate them into our projects.


```c
#include <stdio.h>
```


We will be using the stdio.h (i.e., **standard input/output) **header file very often.

Nitty gritty clarifications of all the other things like header files,  will continue in the later parts


## Header files


* Collection of predefined/built in functions developed for convenience.
* It is always declared on the heading side of the program,always at the top, hence it is called header file.
* It is identified with the extension(.h)
* It gets installed while installing IDE(integrated development environment)
    * In advanced projects, you might create your own header file. Or 'reuse' an existing one.
* It stores functions as per their categories hence they are called libraries.


### Syntax


```c
// Here we include all the header files
#include <stdio.h>

main() {
// All our program statements go inside the main function.
}
```


Here, the first line is a preprocessor command, including a header file, stdio.h.



* C ignores empty lines and spaces.
* There is a `main()` function then, which should always be there. As they say, _Main function is the entry point of the entire program._

A C program is made up of many tokens that have been combined. These tokens consist of:



* Keywords
* Identifiers
* Constants
* String Literal 
* Symbols


## Keywords

Keywords are reserved words that cannot be used to name variables or functions elsewhere in the code. They are only used for the purpose for which they were designed. Their predetermined functions are known.

`return `is one such keyword that is used to create return statements for functions. `auto, if, default,` and others are other examples.

When we enter a keyword into the IDE, the color of that keyword slightly changes, making it stand out from other variables or functions. For instance, in the Turbo C program, all keywords are rendered in white. This feature is called syntax highlighting, another great advantage of using an IDE.


## Identifiers

Variables and functions are given names to distinguish them from one another. Their definitions are entirely up to us, but there are a few guidelines to follow when naming identifiers. One such rule states that the name cannot contain special characters such as @, -, *, and so on.

Because C is a case-sensitive language, an identifier with a capital letter and another with a small letter in the same place will be different. For example, the words Code, code, and cOde can all be used as different identifiers.

Identifier naming guidelines:



* No identifier should be named with a numeric value or a symbol. It should only begin with an underscore or alphabet. 
* There should be no white space in them.
*  Giving logical names is encouraged by our program.

Few valid variable and function names are


```c
inputString, user_input, array1, m_Activate, getColor
```



## Constants

Constants are very similar to variables in that they can be of any data type. The only distinction between a constant and a variable is that the value of a constant does not change. In the following tutorial, we will go over constants in greater depth.

For example, a constant can be a number.


```c
5; 5.04; "A";
```



## String Literal

A string literal, also known as a string constant, is a sequence of characters surrounded by double quotation marks. `"This is a string literal!"` is one example. The C method `printf()` uses the same to format the output.


# C Comments

Comments can be used to insert any informative piece that a programmer does not wish to be executed. It could be either to explain a piece of code or to make it more readable. In addition, it can be used to prevent the execution of alternative code when the process of debugging is done.

Comments can be single-lined or multi-lined.


### Single Line Comments

Single-line comments start with two forward slashes (//). Any information following the slashes // on the same line is ignored (not executed).An example of how we use a single-line comment is 


```c
#include <stdio.h>
 void main()
{
    //This is a single line comment
}
```


 


### Multi-line comments

A multi-line comment begins with /* and ends with */. The compiler ignores any information between /* and */. An example of a multi-line comment


```c
#include <stdio.h>
 
int main()
{
    /* This is a
    multi-line
    comment */
    printf("Hello World!");
    return 0;
}
```


