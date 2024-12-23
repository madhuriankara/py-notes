---
title: Factorial-Of-A-Number
date: 2024-12-23
author: Your Name
cell_count: 8
score: 5
---

```python
def factorial(n):
    """
    Calculate the factorial of a number.

    Parameters:
    n (int): The number to calculate the factorial for.

    Returns:
    int: The factorial of the given number.
    """
    
    # TODO: Implement the factorial calculation here
    if n ==0 or n ==1:
        return 1
        
    result = 1
    for i in range(2,n+1):
        result *= i
    return result
        
```


```python
print(factorial(0)) # Expected output: 1
#print(factorial(5)) # Expected output: 120
#print(factorial(10)) # Expected output: 3628800
```

    1



```python
print(factorial(5)) # Expected output: 120
```

    120



```python
print(factorial(10)) # Expected output: 3628800
```

    3628800



```python

```


```python

```


```python

```


```python

```


---
**Score: 5**
