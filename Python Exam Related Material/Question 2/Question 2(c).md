## Discuss file I/O in Python. Write a Python program to read a file line-by-line and store it into a variable. Explain the following file built-in methods with their clear syntax, description and illustration: read(), readlines(), readline(), tell( ), seek(), write(), writelines().

File I/O (Input/Output) in Python is a crucial aspect for working with files. Python provides several functions and methods to create, read, write, and append to files.

Here's a simple Python program to read a file line-by-line and store it into a variable:

```python
with open('filename.txt', 'r') as file:
    lines = file.readlines()

print(lines)
```

In this code, `'filename.txt'` is the name of the file to be read. The `open()` function is used to open the file in read mode (`'r'`). The `readlines()` method reads all lines in the file and returns them as a list of strings. Each string in the list represents a line in the file.

Now, let's discuss the requested file built-in methods:

1. **read()**: This method reads the entire file and returns it as a single string.
    ```python
    with open('filename.txt', 'r') as file:
        data = file.read()
    ```

2. **readlines()**: This method reads all lines in the file and returns them as a list of strings.
    ```python
    with open('filename.txt', 'r') as file:
        lines = file.readlines()
    ```

3. **readline()**: This method reads the next line of the file and returns it as a string. Each subsequent call to `readline()` will return the next line.
    ```python
    with open('filename.txt', 'r') as file:
        line = file.readline()
    ```

4. **tell()**: This method returns the current file position (in bytes).
    ```python
    with open('filename.txt', 'r') as file:
        pos = file.tell()
    ```

5. **seek(offset, whence)**: This method changes the file position to the given `offset`. The `whence` parameter is optional and defaults to 0, which means absolute file positioning, other values are 1 which means seek relative to the current position and 2 means seek relative to the file's end.
    ```python
    with open('filename.txt', 'r') as file:
        file.seek(10)  # Go to the 10th byte in the file
    ```

6. **write(string)**: This method writes the `string` to the file. If the file was opened in text mode, it must be a string. If the file was opened in binary mode, it must be bytes.
    ```python
    with open('filename.txt', 'w') as file:
        file.write("Hello, World!")
    ```

7. **writelines(list)**: This method writes a list of strings to the file. The strings are concatenated without any separators.
    ```python
    with open('filename.txt', 'w') as file:
        lines = ["Hello, World!", "Welcome to Python."]
        file.writelines(lines)
    ```

Remember, always close the file after you're done with it. The `with` statement does this automatically for you. If you open the file using `open()` without `with`, you should close it manually by calling `file.close()`. Also, handle exceptions and edge cases as per your requirements.
