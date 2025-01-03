---
title: Merging-Dictionaries
date: 2025-01-03
author: Your Name
cell_count: 3
score: 0
---

```python
def merge_dicts(dict1, dict2):
    """
    Merge two dictionaries into one.

    Parameters:
    dict1 (dict): The first dictionary to be merged.
    dict2 (dict): The second dictionary to be merged.

    Returns:
    dict: A new dictionary containing the merged key-value pairs from dict1 and dict2.
    """
    
    # Initialize an empty dictionary to store the merged result
    
    
    # Loop through dict1 and add key-value pairs to the merged_dict
    
        
    # Loop through dict2 and add key-value pairs to the merged_dict

    merged = {**dict1, **dict2}
    return merged
    

# Sample test cases
print(merge_dicts({'a': 1, 'b': 2}, {'c': 3, 'd': 4}))  # Output: {'a': 1, 'b': 2, 'c': 3, 'd': 4}

```

    {'a': 1, 'b': 2, 'c': 3, 'd': 4}



```python
print(merge_dicts({'x': 10, 'y': 20}, {'z': 30}))  # Output: {'x': 10, 'y': 20, 'z': 30}
```

    {'x': 10, 'y': 20, 'z': 30}



```python

```


---
**Score: 0**
