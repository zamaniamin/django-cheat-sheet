# Python Syntax

Python was designed for readability, and has some similarities to the English language with influence from mathematics.
Python uses new lines to complete a command, as opposed to other programming languages which often use semicolons or
parentheses. Python relies on indentation, using whitespace, to define scope; such as the scope of loops, functions and
classes. Other programming languages often use curly-brackets for this purpose.

## Execute Python Syntax

As we learned in the previous page, Python syntax can be executed by writing directly in the Command Line:

```shell
>>> print("Hello, World!")
Hello, World! 
```

Or by creating a python file on the server, using the .py file extension, and running it in the Command Line:

```shell
C:\Users\YourName>python myfile.py 
```

## Python Indentation

Indentation refers to the spaces at the beginning of a code line. Where in other programming languages the indentation
in code is for readability only, the indentation in Python is very important. Python uses indentation to indicate a
block of code. The number of spaces is up to you as a programmer, the most common use is four, but it has to be at least
one.

```python
if 5 > 2:
    print("Five is greater than two!")
```

You have to use the same number of spaces in the same block of code, otherwise Python will give you an error.

```shell title="Syntax Error"
if 5 > 2:
  print("Five is greater than two!")
        print("Five is greater than two!") 
```

## Comments

Comments can be used to explain Python code.  
Comments can be used to make the code more readable.  
Comments can be used to prevent execution when testing code.

Comments starts with a `#`, and Python will ignore them:

```python
# This is a comment
print("Hello, World!")
```

Comments can be placed at the end of a line, and Python will ignore the rest of the line:

```python 
print("Hello, World!")  # This is a comment 
```

A comment does not have to be text that explains the code, it can also be used to prevent Python from executing code:

```python
# print("Hello, World!")
print("Cheers, Mate!") 
```

## Multiline Comments

Python does not really have a syntax for multiline comments. To add a multiline comment you could insert a `#` for each
line:

```python
# This is a comment
# written in
# more than just one line
print("Hello, World!")
```

Or, not quite as intended, you can use a multiline string.  
Since Python will ignore string literals that are not assigned to a variable, you can add a multiline string (triple
quotes) in your code, and place your comment inside it.

```python
"""
This is a comment
written in
more than just one line
"""
print("Hello, World!") 
```

As long as the string is not assigned to a variable, Python will
read the code, but then ignore it, and you have made a multiline comment.

---
source: [w3schools](https://www.w3schools.com)  