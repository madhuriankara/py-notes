---
title: Check-Number-Even-Odd
date: 2025-01-22
author: Your Name
cell_count: 5
score: 5
---

```python
def check_even_odd(num):
    """
    This function checks if a number is even or odd.

    Parameters:
    num (int): The number to be checked.

    Returns:
    str: 'Even' if the number is even, 'Odd' if the number is odd.
    """

    # Check if the number is even or odd
    if num % 2 ==0:
        return "Even"
    return "Odd"

# Sample test cases
print(check_even_odd(2))  # Expected output: 'Even'


```

    Even



```python
print(check_even_odd(3))  # Expected output: 'Odd'
```

    Odd



```python
print(check_even_odd(0))  # Expected output: 'Even'
```

    Even



```python
print(check_even_odd(1)) 
```

    Odd



```python

```


---
**Score: 5**
