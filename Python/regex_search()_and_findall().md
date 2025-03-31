# regex_function_selection_and_None

## What I learned
- search() is enough to verify if the 2 groups of alphanumeric characters exist instead of using findall()
- For verifying the ouput of search(), we use 'result is (not) None'
- For verifying the output of findall(), we use 'len(result)>0'
- None and [](empty list) are **not** considered to be the same
- '==' checks contents of the variables and 'is' checks the addresses of the variables.
```python
import re
def check_character_groups(text):
  result = re.search(r"\w+\s+\w+", text)
  return result is not None

print(check_character_groups("One")) # False
print(check_character_groups("123  Ready Set GO")) # True
print(check_character_groups("username user_01")) # True
print(check_character_groups("shopping_list: milk, bread, eggs.")) # False
```


## Original Answer
```python
import re
def check_character_groups(text):
  result = re.search(r"\w*", text)
  return result is not None

print(check_character_groups("One")) # False
print(check_character_groups("123  Ready Set GO")) # True
print(check_character_groups("username user_01")) # True
print(check_character_groups("shopping_list: milk, bread, eggs.")) # False
```
