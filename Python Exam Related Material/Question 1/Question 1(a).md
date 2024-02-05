## define sequence type, set type and mapping type datatypes with suitable examples.

Sure, let's define these data types:

1. **Sequence Type**: In Python, sequence types include `str`, `list`, `tuple`, etc. They are ordered collections of items, indexed by non-negative integers. Here's an example with a list:
    ```python
    my_list = [1, 2, 3, 4, 5]
    print(my_list[0])  # Output: 1
    ```

2. **Set Type**: A set in Python is an unordered collection of unique elements. Sets are mutable, but the elements contained in the set must be of an immutable type. Here's an example:
    ```python
    my_set = {1, 2, 2, 3, 4}
    print(my_set)  # Output: {1, 2, 3, 4}
    ```

3. **Mapping Type**: Python's only built-in mapping type is the dictionary (`dict`). Dictionaries are unordered collections of key-value pairs. Keys in a dictionary must be unique and immutable. Here's an example:
    ```python
    my_dict = {'name': 'John', 'age': 25}
    print(my_dict['name'])  # Output: John
    ```

In these examples, `my_list` is a sequence type (list), `my_set` is a set type, and `my_dict` is a mapping type (dictionary). Remember to handle exceptions and edge cases as per your requirements. Also, the actual implementation of your code will depend on your specific needs and design choices. This is just a basic example to illustrate the concept.
