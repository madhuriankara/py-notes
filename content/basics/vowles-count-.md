---
title: Vowles-Count-
date: 2025-01-03
author: Your Name
cell_count: 4
score: 0
---

```python
def count_vowels(s):
    """
    This function counts the number of vowels in a given string.
    
    Parameters:
    s (str): A string to count vowels from.
    
    Returns:
    int: The number of vowels in the string.
    """
    
    # Initialize a variable to store the count of vowels
    
    
    # Loop through each character in the string
    
    
    # Return the count of vowels
    vowels = ['a','e','i','o','u']
    count = 0
    for i in vowels:
        count += s.count(i)
    return count

# Test cases
print(count_vowels("hello")) # Expected output: 2
# print(count_vowels("Python")) # Expected output: 1
# print(count_vowels("programming")) # Expected output: 4
```

    2



```python
print(count_vowels("Python")) # Expected output: 1
```

    1



```python
print(count_vowels("programming")) # Expected output: 4
```

    3



```python

```


---
**Score: 0**
