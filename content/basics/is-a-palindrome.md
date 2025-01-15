---
title: Is-A-Palindrome
date: 2025-01-15
author: Your Name
cell_count: 6
score: 5
---

```python
#https://www.geeksforgeeks.org/python-program-check-string-palindrome-not/
```


```python
def is_palindrome(s):
    """
    Problem: Write a function to check if a string is a palindrome.
    
    Args:
    s: input string to be checked
    
    Returns:
    True if the string is a palindrome, False otherwise
    """
    
    # Half-implemented function
    # Implement the logic here
    
    return s == s[:: -1]

# Sample test cases
# print(is_palindrome("racecar"))  # True
# print(is_palindrome("hello"))    # False
# print(is_palindrome("level"))    # True
```


```python
print(is_palindrome("racecar"))
```

    True



```python
print(is_palindrome("hello"))
```

    False



```python
print(is_palindrome("level"))
```

    True



```python

```


---
**Score: 5**
