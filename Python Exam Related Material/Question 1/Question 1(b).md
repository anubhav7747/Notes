## What are the different ways to use range()? Explain using examples.

The `range()` function in Python is used to generate a sequence of numbers over time. It's commonly used in loops to control the number of iterations. Here are the different ways to use `range()`:

1. **`range(stop)`**: Generates a sequence of numbers starting from `0` up to `stop - 1`.
    ```python
    for i in range(5):
        print(i)
    # Output: 0, 1, 2, 3, 4
    ```

2. **`range(start, stop)`**: Generates a sequence of numbers starting from `start` up to `stop - 1`.
    ```python
    for i in range(2, 5):
        print(i)
    # Output: 2, 3, 4
    ```

3. **`range(start, stop, step)`**: Generates a sequence of numbers starting from `start`, incrementing by `step`, up to `stop - 1`.
    ```python
    for i in range(0, 10, 2):
        print(i)
    # Output: 0, 2, 4, 6, 8
    ```

In these examples, `start`, `stop`, and `step` are integers. `start` and `step` are optional parameters. If not provided, `start` defaults to `0` and `step` defaults to `1`. The `range()` function only works with integer values. If you need to generate a range with decimal numbers, you might need to use a different approach, such as using the `numpy` library's `arange()` or `linspace()` functions. Remember to handle exceptions and edge cases as per your requirements. Also, the actual implementation of your code will depend on your specific needs and design choices. This is just a basic example to illustrate the concept.
