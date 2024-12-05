---
title: Question6
date: 2024-12-05
author: Your Name
cell_count: 3
score: 0
---

def rotate_list(lst, k):
    """
    Rotate a list by k positions.

    Args:
    lst: list - the list to rotate
    k: int - the number of positions to rotate

    Returns:
    list - the rotated list
    """

    # TODO: Implement the rotation logic here
    pass

# Sample test cases
# print(rotate_list([1, 2, 3, 4, 5], 2))  # Output: [4, 5, 1, 2, 3]
# print(rotate_list(['a', 'b', 'c', 'd', 'e'], 3))  # Output: ['c', 'd', 'e', 'a', 'b']
```


```python
def rotate_list(lst, k): 
    lst = lst[3:] + lst[:k+1]
    print ("List after left rotate by 3 : " + str(lst))
    





print(rotate_list([1, 2, 3, 4, 5], 2)) # Output: [4, 5, 1, 2, 3]
```

    List after left rotate by 3 : [4, 5, 1, 2, 3]
    None



```python

```


---
**Score: 0**
