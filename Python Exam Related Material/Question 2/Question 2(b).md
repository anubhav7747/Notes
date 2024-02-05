## What are the differences between abstract class and interface? Illustrate with Python code. Can we instantiate an abstract class? Write a program in which Maruti, Chevrolet and Santro sub classes implement the abstract methods of the super class Car.

An **abstract class** and an **interface** are two types of "incomplete" classes that serve as blueprints for creating more specific, complete classes. Here are some differences between them:

1. **Definition**: An abstract class is a class that contains at least one abstract method (a method declared, but not implemented). An interface is a completely "abstract class" that contains only abstract methods.

2. **Inheritance**: A class can extend only one abstract class while it can implement multiple interfaces.

3. **Methods**: Abstract classes can have non-abstract methods (methods with implementations) while interfaces can have only abstract methods in many languages. However, since Python 3.8, protocols (which are similar to interfaces in other languages) can include concrete methods.

4. **Variables**: Abstract classes can have instance variables. An interface (or protocol in Python) cannot have instance variables.

In Python, we use the `abc` module to create abstract classes. Here's an example:

```python
from abc import ABC, abstractmethod

class Car(ABC):
    @abstractmethod
    def model(self):
        pass

class Maruti(Car):
    def model(self):
        return "Maruti"

class Chevrolet(Car):
    def model(self):
        return "Chevrolet"

class Santro(Car):
    def model(self):
        return "Santro"

# Instantiate the subclasses
maruti = Maruti()
chevrolet = Chevrolet()
santro = Santro()

# Call the model method
print(maruti.model())
print(chevrolet.model())
print(santro.model())
```

In this code, `Car` is an abstract class with an abstract method `model`. `Maruti`, `Chevrolet`, and `Santro` are subclasses that implement the `model` method. We can instantiate the subclasses and call the `model` method on these instances.

However, we **cannot instantiate an abstract class**. If we try to create an instance of `Car`, we will get a `TypeError` because `Car` is an abstract class and cannot be instantiated. This is a key feature of abstract classes: they exist to be extended, but not instantiated. They define a common interface for their subclasses.
