# iterating_with_next()_function

## What I learned
- I can skip the first item simply by using the 'next()' function.
- **'next()'** advances iterator to the next item. 
- Other ways to skip the first item include 'slicing' and 'counter'

```python
import os
import csv

def create_file(filename):
    with open(filename, "w") as file:
        file.write("name,color,type\n")
        file.write("carnation,pink,annual\n")
        file.write("daffodil,yellow,perennial\n")
        file.write("iris,blue,perennial\n")
        file.write("poinsettia,red,perennial\n")
        file.write("sunflower,yellow,annual\n")

def contents_of_file(filename):
    return_string = ""
    create_file(filename)
    with open(filename) as f:
        rows = csv.reader(f)
        next(rows)  # Skip the header row
        for row in rows:
            name, color, type = row
            return_string += "a {} {} is {}\n".format(color, name, type)
    return return_string

print(contents_of_file("flowers.csv"))
```


## Original Answer
```python
import os
import csv

def create_file(filename):
    with open(filename, "w") as file:
        file.write("name,color,type\n")
        file.write("carnation,pink,annual\n")
        file.write("daffodil,yellow,perennial\n")
        file.write("iris,blue,perennial\n")
        file.write("poinsettia,red,perennial\n")
        file.write("sunflower,yellow,annual\n")

def contents_of_file(filename):
    return_string = ""
    create_file(filename)
    with open(filename) as f:
        rows = csv.reader(f)
        for row in rows:
          if "name" not in row:
            name, color, type = row
            return_string += "a {} {} is {}\n".format(color, name, type)
    return return_string

print(contents_of_file("flowers.csv"))
```
