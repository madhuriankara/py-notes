---
title: Check-If-It-Is-Prime
date: 2024-12-23
author: Your Name
cell_count: 5
score: 5
---

```python
def is_prime(num):
    """
    Check if a number is prime.

    Parameters:
    num (int): The number to check for primality.

    Returns:
    bool: True if the number is prime, False otherwise.
    """
    for n in range( 2, int(num**0.5)+1):   
        if (num % n) == 0:
            return False
        return True

# Sample test cases
# print(is_prime(5)) # Expected output: True
# print(is_prime(10)) # Expected output: False
# print(is_prime(17)) # Expected output: True
```


```python
print(is_prime(5)) # Expected output: True
```

    True



```python
print(is_prime(10)) # Expected output: False
```

    False



```python
 print(is_prime(17)) # Expected output: True
```

    True



```python

```


---
**Score: 5**
