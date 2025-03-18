# list_total_length_counting_elements

## What I learned
- **len()** should be used instead of **count()** to calculate the total elements in lists
```python
def string_words(string):
    string_list = string.split()
    result = len(string_list)

    # Complete the return statement using both a string operation and 
    # a string method in a single line.
    return result
```

## Original Answer
```python
def string_words(string):
    string_list = string.split()
    result = count(string_list)

    # Complete the return statement using both a string operation and 
    # a string method in a single line.
    return result
```
