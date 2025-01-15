---
title: Largest-Three-Numbers
date: 2025-01-15
author: Your Name
cell_count: 4
score: 0
---

```python
#Find the three largest numbers in a list
```


```python
def find_largest_three_numbers():
    lst = [4,7,8,9,1,2]
    largest = sorted(lst, reverse = True)[:-3]
    return largest
        
```


```python
find_largest_three_numbers()
```




    [9, 8, 7]




```python

```


---
**Score: 0**
