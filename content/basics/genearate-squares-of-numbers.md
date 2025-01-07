---
title: Genearate-Squares-Of-Numbers
date: 2025-01-06
author: Your Name
cell_count: 3
score: 0
---

```python
def generate_squares(n):
    """
    Generate a list of squares of numbers from 1 to n.

    Parameters:
    n (int): The upper limit of the range.

    Returns:
    list: A list of squares of numbers from 1 to n.
    """
    return [x ** 2 for x in range(1,n+1) ]
        

# Sample test cases
print(generate_squares(5)) # Expected output: [1, 4, 9, 16, 25]

```

    [1, 4, 9, 16, 25]



```python
print(generate_squares(3)) # Expected output: [1, 4, 9]
```

    [1, 4, 9]



```python

```


---
**Score: 0**
