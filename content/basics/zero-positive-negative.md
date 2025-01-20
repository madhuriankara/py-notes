---
title: Zero-Positive-Negative
date: 2025-01-20
author: Your Name
cell_count: 4
score: 0
---

```python
def check_number(num):
    """
    This function checks if a number is positive, negative, or zero.

    Parameters:
    num (int): The number to be checked.

    Returns:
    str: 'Positive' if the number is positive, 'Negative' if the number is negative, 'Zero' if the number is zero.
    """
    
    # Implement the function here
    if num < 0:
        return "Negative"
    if num == 0:
        return "zero"
    if num > 0:
        return "Positive"

# Sample test cases
print(check_number(5))  # Expected output: 'Positive'


```

    Positive



```python
print(check_number(-3))  # Expected output: 'Negative'
```

    Negative



```python
print(check_number(0))  # Expected output: 'Zero'
```

    zero



```python

```


---
**Score: 0**
