# File I/O

In C, file input/output (I/O) is a method of interacting with files on the computer's hard drive or other storage devices. It lets you read data from and write data to files, which is a useful feature for many programmes.


## Opening and Closing Files

To begin working with a file in C, you must first open it. The fopen() function opens a file and returns the file's pointer. Here's an illustration:


```c
FILE *fp;
fp = fopen("file.txt", "r");
```


This code reads a file called file.txt ("r" mode). fopen() will return NULL if the file does not exist.

When you're finished with a file, use the fclose() function to close it, as shown below:


```c
fclose(fp);
```



## Reading and Writing to Files

To read data from a file, use functions such as fscanf() or fgets(). Here's an example:


```c
int num;
fscanf(fp, "%d", &num);
```


fscanf() is used in this code to read an integer from the file fp.

You can use functions like fprintf() or fputs() to write data to a file. As an example, consider the following:


```c
fprintf(fp, "Hello, world!");
```


fprintf() is used in this code to write the string "Hello, world!" to the file fp.


## File Modes

When you open a file in C, you can specify a file mode, which controls how the file is used. There are several file modes to choose from, including:



* "**r": Read mode:** Opens a file for reading only.
* **"w": Write mode:** Opens a file for writing only. If the file does not exist, it will be created. If it exists, its contents will be erased.
* **"a": Append mode:** Opens a file for writing only. If the file does not exist, it will be created. If it exists, data will be appended to the end of the file.
* **"rb", "wb", "ab": Binary modes:** These modes are similar to the above modes, but they are used for binary file I/O.


## Binary File I/O

Binary file I/O is a method of reading and writing binary data to and from files. Because binary file I/O can be faster than text file I/O, it is frequently used for performance reasons.

You can use functions like fread() and fwrite() to read and write binary data. Here's an illustration:


```c
struct Person {
    char name[50];
    int age;
    float height;
};

struct Person p;

FILE *fp;
fp = fopen("people.bin", "wb");

fwrite(&p, sizeof(struct Person), 1, fp);
```


This code saves the p structure to the binary file people.bin.

To read binary data, use fread() as follows:


```c
fread(&p, sizeof(struct Person), 1, fp);
```


This code reads from the file fp one Person structure.

File I/O is a feature of programming languages such as C that allows you to interact with files on the computer's hard drive or other storage devices. Understanding file I/O is required when writing programmes that read from or write to files, and it can be a powerful tool for data processing.
