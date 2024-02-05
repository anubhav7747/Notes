## Write a Python program to create a class 'Student' with members: name, class, branch, grade. Use appropriate constructor and destructor in your program. Define the member functions for reading and displaying the student's information.

Sure, here is a Python program that defines a `Student` class with the requested members and methods:

```python
class Student:
    def __init__(self, name, class_, branch, grade):
        self.name = name
        self.class_ = class_
        self.branch = branch
        self.grade = grade

    def __del__(self):
        print(f"Destructor called, {self.name} is deleted.")

    def read_info(self):
        self.name = input("Enter student's name: ")
        self.class_ = input("Enter student's class: ")
        self.branch = input("Enter student's branch: ")
        self.grade = input("Enter student's grade: ")

    def display_info(self):
        print(f"Name: {self.name}")
        print(f"Class: {self.class_}")
        print(f"Branch: {self.branch}")
        print(f"Grade: {self.grade}")

# Create a student object
student1 = Student("John Doe", "10th", "Science", "A")

# Display student information
student1.display_info()

# Read new information and update the student object
student1.read_info()

# Display updated information
student1.display_info()
```

In this program, the `Student` class has four data members: `name`, `class_`, `branch`, and `grade`. The `__init__` method is the constructor that initializes these members when a `Student` object is created. The `__del__` method is the destructor that gets called when the object is about to be destroyed.

The `read_info` method reads the student's information from the user, and the `display_info` method prints the student's information. Please note that this code will not run in an online compiler as it requires user input. You can run it in your local environment. Also, remember to handle exceptions and edge cases as per your requirements.
