---
title: Swapped Values
date: 2024-11-20
author: Your Name
cell_count: 4
score: 0
---

Takes two variables.
Swaps their values without using a third variable.
Prints the swapped values.


```python
def swap_two_variables():
    a=10
    b=20
    a,b = b,a
    result = (a,b)
    return f'The {result} is now swapped'
    
```


```python
swap_two_variables()
```




    'The (20, 10) is now swapped'




```python

```


---
**Score: 0**
