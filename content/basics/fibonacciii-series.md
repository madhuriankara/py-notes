---
title: Fibonacciii-Series
date: 2025-01-13
author: Your Name
cell_count: 2
score: 0
---

```python
def fibonacci_numbers(n):
    #Problem: Write a function to return the first n Fibonacci numbers.
    
    #Parameters:
    #n (int): Number of Fibonacci numbers to return
    
    #Returns:
    #list: List of the first n Fibonacci numbers
    
    
    # Initialize the list to store Fibonacci numbers
    fib = [0,1]
    for i in range(2,n):
        fib.append(fib[i-1] + fib[i-2])
    return fib[:n]


# Sample test cases
print(fibonacci_numbers(0))  # Output: []
print(fibonacci_numbers(1))  # Output: [0]
print(fibonacci_numbers(5))  # Output: [0, 1, 1, 2, 3]
```

    []
    [0]
    [0, 1, 1, 2, 3]



```python

```


---
**Score: 0**
