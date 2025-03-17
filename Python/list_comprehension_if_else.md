# list_comprehension_if_else_syntax

## What I learned
- there is a way to return the values for the elements that doesn't meet the condition
- this is a **if-else** statement I learned below

```python
[값1 if 조건 else 값2 for 변수 in 반복가능한객체]
```
```python
filenames = ["program.c", "stdio.hpp", "sample.hpp", "a.out", "math.hpp", "hpp.out"]
new_filenames = [x.replace("hpp","h") if x.endswith("hpp") **else x** for x in filenames] 
```


## Original Answer
```python
filenames = ["program.c", "stdio.hpp", "sample.hpp", "a.out", "math.hpp", "hpp.out"]
new_filenames = [x.replace("hpp","h") for x in filenames if x.endswith("hpp")] 
```
