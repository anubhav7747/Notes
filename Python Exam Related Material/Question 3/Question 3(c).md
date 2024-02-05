## What is Exception? Explain about the different types of Exceptions in Python and discuss when do they occur. Demonstrate the use of Exception Handling in Python. How to create, raise and handle user defined exceptions in Python? Illustrate with a suitable program.

An **Exception** is an event that occurs during the execution of a program, disrupting the normal flow of the program's instructions. In Python, exceptions are triggered automatically on errors, or they can be triggered and intercepted by your code.

Python has several built-in exceptions, such as `IndexError`, `TypeError`, `ValueError`, `FileNotFoundError`, and many more. These exceptions are raised when related errors occur. For example, `IndexError` is raised when you try to access an index that does not exist in a list, and `TypeError` is raised when an operation or function is applied to an object of inappropriate type.

Here's an example of exception handling in Python:

```python
try:
    # This code might raise an exception
    x = 1 / 0
except ZeroDivisionError:
    # This code will be executed if there is a ZeroDivisionError
    print("You can't divide by zero!")
```

In this code, the `try` block contains code that might raise an exception. The `except` block contains code that will be executed if a specific exception (in this case, `ZeroDivisionError`) is raised in the `try` block.

You can also define your own exceptions in Python by creating a new class that inherits from the `Exception` class or one of its subclasses. Here's an example:

```python
class MyException(Exception):
    pass

try:
    # This code raises an exception
    raise MyException("This is a custom exception")
except MyException as e:
    # This code will be executed if there is a MyException
    print(e)
```

In this code, `MyException` is a user-defined exception. The `raise` statement is used to raise the `MyException`. The string passed to `MyException` is the error message that will be displayed when the exception is printed. Remember to handle exceptions and edge cases as per your requirements. Also, the actual implementation of your exceptions will depend on your specific needs and design choices. This is just a basic example to illustrate the concept.
