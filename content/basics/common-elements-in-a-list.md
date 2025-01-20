---
title: Common-Elements-In-A-List
date: 2025-01-20
author: Your Name
cell_count: 4
score: 0
---

```python
#https://stackoverflow.com/questions/2864842/common-elements-comparison-between-2-lists
```


```python
def find_common_elements(list1, list2):
    """
    Problem: Write a function to find the common elements in two lists.

    Args:
    list1: First list of elements
    list2: Second list of elements

    Returns:
    List of common elements between list1 and list2
    """

    # Initialize an empty list to store common elements
    result = []
    for i in list1:
        if i in list2:
            result.append(i)
    return result

# Sample test cases
print(find_common_elements([1, 2, 3, 4, 5], [4, 5, 6, 7, 8]))  # Output should be [4, 5]

```

    [4, 5]



```python
print(find_common_elements([1, 2, 3], [4, 5, 6]))  # Output should be []
```

    []



```python

```


---
**Score: 0**
