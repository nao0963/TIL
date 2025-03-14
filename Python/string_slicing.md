# string_slicing_error

## What I Learned
- I learned that '**[::-1]**' means counting every letter in the String from the back to the front
- since no number before and after the colon indicates counting from the first to the last without slicing out anything
- and -1 means the way of counting, in this case counting from back.

## Quiz & Answer
```python
def is_palindrome(input_string):

    new_string = ""
    reverse_string = ""

    for letter in input_string :
        if letter != " ":
            new_string = new_string + letter.lower()
            reverse_string = new_string[::-1]

    if new_string == reverse_string :
        return True
    return False

print(is_palindrome("Never Odd or Even")) # Should be True
print(is_palindrome("abc")) # Should be False
print(is_palindrome("kayak")) # Should be True
```
