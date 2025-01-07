---
title: Remove-Duplicates-List
date: 2025-01-06
author: Your Name
cell_count: 4
score: 0
---

```python
#https://www.geeksforgeeks.org/python-ways-to-remove-duplicates-from-list/
```


```python
def remove_duplicates(lst):
    """
    Problem: Write a function to remove duplicates from a list.
    
    Args:
    lst: a list of elements
    
    Returns:
    a list with duplicates removed
    """
    
    # initialize an empty list to store unique elements
    
    # loop through the input list
    
    lst = list(dict.fromkeys(lst))
    return lst
    

# Sample test cases
print(remove_duplicates([1, 2, 2, 3, 4, 4, 5])) # Output: [1, 2, 3, 4, 5]
# print(remove_duplicates(['a', 'b', 'a', 'c', 'd', 'b'])) # Output: ['a', 'b', 'c', 'd']
```

    [1, 2, 3, 4, 5]



```python
print(remove_duplicates(['a', 'b', 'a', 'c', 'd', 'b'])) # Output: ['a', 'b', 'c', 'd']
```

    ['a', 'b', 'c', 'd']



```python

```


---
**Score: 0**
