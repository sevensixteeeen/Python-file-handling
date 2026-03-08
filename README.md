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

## Open a file on the server
Assume we have the following file, located in the same folder as Python.

**Domofile.txt**
```Python
Hello! Welcome to demofile.txt
This file is for testing purposes.
Working….
```

To open the file, use the bulit-in open() function.

The open() function return a file object, Which has a read() method for reading the content of the file:

**Ex:**
```Python
f=open("demofile.txt")
print(f.read())     
```

If the file is located in a different location, you will have to specify the file path, like this:

**EX:**

```Python
f = open("D:\\myfiles\welcome.txt")
print(f.read())
```

## Using with statement 
you can also use the with statement when opening a file.

**Ex:**

```Python
with open("demofile.txt") as f:
print(f.read())
```

Then you do not have to worry about closing your files, the with statement takes care of that.

## Close Files

It is a good practice to always close the file when you are done with it.

If you are not using the with statement, you must write a close statement in order to close the file:

**Ex:**
```Python
f = open("demofile.txt")
print(f.readline())
f.close()
```
Note: You should always close your files. In some cases, due to buffering, changes made to a file may not show until you close the file.

## Read only parts of the file
By default the read() method returns the whole text, but you can also specify how many characters you want to return:

**Ex:**
```Python
with open("demofile.txt") as f:
  print(f.read(5))
```

## Read Lines 

You can return one line by using the readline() method:

**Ex:**
```Python
with open("demofile.txt") as f:
  print(f.readline())
```

By calling readline() two times, you can read the two first lines:

**Ex:**
```Python
with open("demofile.txt") as f:
  print(f.readline())
  print(f.readline())
```

By looping through the lines of the file, you can read the whole file, line by line:

**Ex:**
```Python
with open("demofile.txt") as f:
  for x in f:
    print(x)
```
# Python File write

## Write to an existing file
To write to an existing file, you must add a parameter to the open() function:

"a" -Append - will append to the end of the file

"w" - Write - will overwrite any existing content

**Ex:**
```Python
with open("demofile.txt", "a") as f:
  f.write("Now the file has more content!")

#open and read the file after the appending:
with open("demofile.txt") as f:
  print(f.read())
```

