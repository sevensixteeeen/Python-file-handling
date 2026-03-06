# Python file handling
File handling is an important part of any web application.

Python has several functions for creating, reading, updating, and deleting files.

## File Handling
The key function for working with files in Python in the open(.) function.

The open(.) function takes two parameters; filename, and mode.

There are four different methods (modes) for opening a file:

```
"r"- Read -  Default value. opens a file for reading, error if the file does not exist.

"a"- append - Opens a file for appending, creating the file if it does not exist.

"w"- write - Opens a file for writing, creates the file if it does not exist.

"x"- create - creates the specified file, returns an error if the file exists.

```

Python has several functions for creating, reading, updating, and deleting files.

```
"t" - Text - Default value. Text mode

"b" - Binary - Binary mode (e.g. images)
```

## Syntax
The open a file for reading it is enough to specify the name of the file:

```Python
f=open("demofile.txt")
```

The code above is the same as:

```Python
f=open("demofile.txt","rt")
```

Because "r" for read, and "t" for text are the default values, you do not need to specify them.

Note: Make sure the file exists, or else you will get an error.

## Open a file on the 
Assume we have the following file, located in the same folder as Python.

**Domofile.txt**
```
Hello! Welcome to demofile.txt
This file is for testing purposes.
Working….
```

To open the file, use the bulit-in open() function.

The open() function return a file object, Which has a read() method for reading the content of the file:

**Ex:**
```
f=open("demofile.txt")
print(f.read())     
```

If the file is located in a different location, you will have to specify the file path, like this:

