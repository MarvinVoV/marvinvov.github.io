---
layout: page
permalink: /python/function
categories:
  - python
---

## Default Argument values

The default values are evaluated at the point of function definition in the defining scope. 
```python
i = 5
def f(arg = i):
	print(arg)

i = 6

f()
```
will print 5.