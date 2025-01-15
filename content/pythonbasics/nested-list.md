---
title: Nested-List
date: 2025-01-15
author: Your Name
cell_count: 3
score: 0
---

```python
#Flatten a nested list
```


```python
def nested_list():
    lst = [[1, 2, 3], [4, 5], [6]]
    a = tuple(i for sublist in lst for i in sublist) 
    return a 
nested_list()
```




    (1, 2, 3, 4, 5, 6)




```python

```


---
**Score: 0**
