---
title: Divisibility
date: 2024-12-02
author: Your Name
cell_count: 8
score: 5
---

10
Takes a number 
Checks if it is divisible by both 5 and 3.
Prints "Divisible by both" or "Not divisible by both."


```python
def get_divisibility(i):
        if i % 3 ==0 and i % 5 == 0:
            return f' The number {i} is divisible by 3 and 5'
        else:
            return f'The number {i} is not divisible by 3 and 5'
```


```python
get_divisibility(30)
```




    ' The number 30 is divisible by 3 and 5'




```python

```


```python
get_divisibility(22)
```




    'The number 22 is not divisible by 3 and 5'




```python

```


```python
get_divisibility(40)
```




    'The number 40 is not divisible by 3 and 5'




```python

```


---
**Score: 5**
