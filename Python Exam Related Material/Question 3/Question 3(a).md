## Give a taxonomy to represent the types of Polymorphism in Python. Differentiate between method overloading and method overriding with example. Write down a program in Python for addition of the two complex numbers using operator overloading.

Polymorphism in Python can be broadly classified into two types:

1. **Compile Time Polymorphism (Static Binding)**: This is achieved by method overloading and operator overloading.
2. **Run Time Polymorphism (Dynamic Binding)**: This is achieved by method overriding.

**Method Overloading**: In Python, we can define a method in such a way that there are multiple ways to call it. Given a single method or function, we can specify the number of parameters ourselves. Depending on the function definition, it can be called with zero, one, two or more parameters. This is known as method overloading. Not all programming languages support method overloading, but Python does.

Example:
```python
def add(a, b):
    return a + b

def add(a, b, c):
    return a + b + c
```
In the above code, we have two `add` methods, but we can only use the second one, as Python does not support method overloading. We may define many methods of the same name and different argument but we can only use the latest defined method.

**Method Overriding**: If a child class provides a specific implementation of a method that is already provided by its parent class, it is known as method overriding. Overriding is a very important part of OOP since it is an example of run time polymorphism.

Example:
```python
class Parent:
    def method(self):
        print("This is from the parent class")

class Child(Parent):
    def method(self):
        print("This is from the child class")

c = Child()
c.method()
```
In the above code, we have two `method` methods. When we call `c.method()`, the method from the child class is called because the child class overrides the `method` of the parent class.

Now, let's write a Python program for the addition of two complex numbers using operator overloading:

```python
class Complex:
    def __init__(self, real, imag):
        self.real = real
        self.imag = imag

    def __add__(self, other):
        real = self.real + other.real
        imag = self.imag + other.imag
        return Complex(real, imag)

    def __str__(self):
        return f"{self.real} + {self.imag}i"

# Create two Complex numbers
c1 = Complex(1, 2)
c2 = Complex(2, 3)

# Add the two Complex numbers
c3 = c1 + c2

# Print the result
print(c3)
```
In this program, the `Complex` class defines the `__add__` method to add two `Complex` numbers. The `__str__` method is used to display the `Complex` number in the form "a + bi". When we use the `+` operator to add two `Complex` numbers, the `__add__` method is called. This is an example of operator overloading. The `+` operator is overloaded by the `__add__` method. The `__str__` method is used to convert the object into a string for printing. It is an example of method overriding as it overrides the `__str__` method of the base `object` class. Remember to handle exceptions and edge cases as per your requirements.
