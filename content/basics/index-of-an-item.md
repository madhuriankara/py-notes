---
title: Index-Of-An-Item
date: 2025-01-03
author: Your Name
cell_count: 3
score: 0
---

```python
def find_index(item, lst):
    """
    This function finds the index of an item in a list.

    Parameters:
    item (any): The item to find in the list.
    lst (list): The list to search for the item.

    Returns:
    int: The index of the item in the list, or -1 if the item is not found.
    """

    # TODO: Implement the function here
    try:
        index = lst.index(item)    
        if item in lst:
            return index
    except:
        return -1


# Sample test cases
print(find_index(3, [1, 2, 3, 4, 5]))  # Expected output: 2
print(find_index('a', ['a', 'b', 'c']))  # Expected output: 0
print(find_index(6, [1, 2, 3, 4, 5]))  # Expected output: -1
```

    2
    0
    -1



```python

```


```python

```


---
**Score: 0**
