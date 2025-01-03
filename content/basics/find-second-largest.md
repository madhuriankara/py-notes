---
title: Find-Second-Largest
date: 2025-01-03
author: Your Name
cell_count: 4
score: 0
---

```python
def find_second_largest(arr):
    """
    Given a list of integers, find the second largest number in the list.

    Parameters:
    arr (list): A list of integers

    Returns:
    int: The second largest number in the list
    """
    
    # Sort the list in descending order
    
    
    # Return the second element in the sorted list
    arr.sort()
    return arr[-2]
    

# Sample test cases
print(find_second_largest([1, 2, 3, 4, 5])) # Expected output: 4
# print(find_second_largest([10, 5, 20, 15, 30])) # Expected output: 20
```

    4



```python
print(find_second_largest([10, 5, 20, 15, 30])) # Expected output: 20
```

    20



```python
print(find_second_largest([10, 5, 25, 82, 30]))
```

    30



```python

```


---
**Score: 0**
