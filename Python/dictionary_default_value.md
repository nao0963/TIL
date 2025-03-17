# dictionary_default_value_setting_syntax

## What I Learned
- **dictionary[key].append(value)** is used for adding value to the key in dictionary.
- when adding value, there are ways to prevent/avoid Keyerror. 
    - using **setdefault()** 
        - ```python 
          my_dict = {"a": [1, 2], "b": [3, 4]}
          my_dict.setdefault("c", []).append(5)  # 'c'가 없으면 빈 리스트 [] 추가 후 append
          print(my_dict)
          ```
    - using **defaultdict** by importing **collections** module
        - ```python
          from collections import defaultdict
          my_dict = defaultdict(list)  # 기본값을 리스트([])로 설정
          my_dict["c"].append(5)  # 'c'가 없어도 자동으로 빈 리스트 생성 후 append
          print(my_dict)
          ```
- The methods above ensure there is a list to append even if the key specified doesn't exist!!


## Original Answer
```python
if user not in user_groups:
  user_groups[user] = []
user_groups[user].append(group)
```
