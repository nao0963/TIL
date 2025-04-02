# regex_whitespace_character_usage

## What I learned
- a space preceding the zip code can be represented by **\s**
- preceding **\s** can restrict the matches that starts from the beginning of text(as required by direction)
```python
import re
def correct_function(text):
 result = re.search(r"\s+\d{5}(-\d{4})?\b", text)
 return result != None

def check_zip_code(text):
  return correct_function(text)  

print(check_zip_code("The zip codes for New York are 10001 thru 11104.")) # True
print(check_zip_code("90210 is a TV show")) # False
print(check_zip_code("Their address is: 123 Main Street, Anytown, AZ 85258-0001.")) # True
print(check_zip_code("The Parliament of Canada is at 111 Wellington St, Ottawa, ON K1A0A9.")) # False
```


## Original Answer
```python
import re
def correct_function(text):
 result = re.search(r"\d{5}(-\d{4})?", text)
 return result != None

def check_zip_code(text):
  return correct_function(text)  

print(check_zip_code("The zip codes for New York are 10001 thru 11104.")) # True
print(check_zip_code("90210 is a TV show")) # False
print(check_zip_code("Their address is: 123 Main Street, Anytown, AZ 85258-0001.")) # True
print(check_zip_code("The Parliament of Canada is at 111 Wellington St, Ottawa, ON K1A0A9.")) # False
```
