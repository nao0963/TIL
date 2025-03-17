# list_comprehension_nested_for_loops

## What I Learned
- list comprehension could be also used for executing nested for loops
- This can be done by writing for loops one after another. 
  ```python 
  def email_list(domains):
  return [f"{user}@{domain}" **for** domain, users in domains.items() **for** user in users]
  ```
- This made my function more concise compared to the one used before knowing it just as below.


## Original Answer
```python
def email_list(domains):
	emails = []
	for domain, users in domains.items():
	  for user in users:
	    emails.append(f"{user}@{domain}")
	return emails
```
