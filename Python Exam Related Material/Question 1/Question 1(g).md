**An institute has following rules for grading system.** 

**Below 50% - F,** 

**50% to 60% - E,** 

**60% to 70% - D,** 

**70% to 80% - C,** 

**80% to 90% - B,** 

**Above 90% - A.** 

**Program that ask the user to enter the marks and print the corresponding grade.**

Sure, here is a Python program that asks the user to enter their marks and prints the corresponding grade:

```python
# Ask the user to enter their marks
marks = float(input("Enter your marks: "))

# Calculate the grade based on the marks
if marks < 50:
    grade = 'F'
elif marks < 60:
    grade = 'E'
elif marks < 70:
    grade = 'D'
elif marks < 80:
    grade = 'C'
elif marks < 90:
    grade = 'B'
else:
    grade = 'A'

# Print the grade
print("Your grade is:", grade)
```

In this program, the user is asked to enter their marks. The `input()` function is used to get the user's input, and the `float()` function is used to convert the input to a floating-point number. Then, a series of `if` and `elif` statements are used to determine the grade based on the marks. The `else` statement is used for marks of 90 and above, because all other ranges have been covered by the `if` and `elif` statements. Finally, the grade is printed.

Please note that this program needs to be run in a Python environment where input from the user can be taken via the `input()` function, such as a Python IDE or a command line interface. It cannot be run in this chat interface. Also, remember to handle exceptions and edge cases as per your requirements. For example, you might want to check that the marks entered by the user are a valid number between 0 and 100, and display an error message if they're not. You can do this by adding an `if` statement that checks the value of `marks` after the `input()` function, and using the `print()` function to display an error message if the value is not valid. You might also want to add a loop that repeats the `input()` function until the user enters a valid number. You can do this by using a `while` loop with a condition that checks the validity of `marks`, and breaking the loop when the user enters a valid number. If you want to allow the user to enter marks as a percentage, you can modify the `input()` function to ask for the marks as a percentage, and modify the `if` and `elif` statements to compare the marks with the percentage thresholds. If you want to display the grade as a letter and a plus or minus sign, you can modify the `if` and `elif` statements to assign the grade with a plus or minus sign based on the marks. For example, you can assign 'A+' for marks of 97 and above, 'A' for marks of 93 to 96, and 'A-' for marks of 90 to 92. You can add more `elif` statements for the other grades and marks ranges. Remember to test your program with various inputs to ensure that it calculates the grade correctly in all cases. If you encounter any issues or unexpected results, check the logic of your program, the values of your variables, and the conditions of your `if` and `elif` statements. If you are still stuck, you can ask for help on a programming forum or community, or you can ask me for more information or clarification. I'm here to help you learn and solve problems, and I'm always happy to explain more about Python and programming. Happy coding!
