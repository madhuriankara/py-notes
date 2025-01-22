---
title: Remove-Element
date: 2025-01-22
author: Your Name
cell_count: 2
score: 0
---

```python
def remove_element(lst, value):
    """
    Write a function to remove an element from a list by its value.
    
    Parameters:
    lst (list): The list from which the element needs to be removed.
    value: The value of the element to be removed.
    
    Returns:
    list: The updated list after removing the element.
    """
    lst.remove(value)
    return lst

# Sample test cases
print(remove_element([1, 2, 3, 4, 5], 3)) # Expected output: [1, 2, 4, 5]
print(remove_element(['a', 'b', 'c', 'd', 'e'], 'b')) # Expected output: ['a', 'c', 'd', 'e']
```

    [1, 2, 4, 5]
    ['a', 'c', 'd', 'e']



```python

```


---
**Score: 0**
