---
title: Check-If-Leap-Year-Or-Not
date: 2025-01-13
author: Your Name
cell_count: 6
score: 5
---

```python
def is_leap_year(year):
    """
    Given a year, check if it is a leap year.

    Parameters:
    year (int): The year to be checked.

    Returns:
    bool: True if the year is a leap year, False otherwise.
    """

    # Check if the year is divisible by 4
    if year % 400 == 0 :
        return True
    return False

# Sample test cases
print(is_leap_year(2000)) # Expected output: True
# print(is_leap_year(1900)) # Expected output: False
# print(is_leap_year(2021)) # Expected output: False
```

    True



```python
print(is_leap_year(1900)) # Expected output: False
```

    False



```python
print(is_leap_year(2021)) # Expected output: False
```

    False



```python
print(is_leap_year(1996))
```

    True



```python
print(is_leap_year(2044)) 
```

    True



```python

```


---
**Score: 5**
