---
title: Small Large
date: 2025-01-13
author: Your Name
cell_count: 9
score: 5
---

Finds and prints the smallest and largest numbers in the list.


```python
def get_large_small(i):
    if i <= 2:
        print("The number is smallest")
    else:
        print("The number is largest")
```


```python
get_large_small(0)
```

    The number is smallest



```python

```


```python
get_large_small(10)
```

    The number is largest



```python

```


```python
def get_large_small(i):
    numbers = [2, 4, 6, 8, 10]
    
    if i in numbers:
        if i <= 2:
            return f'The number {i} is the smallest'
        else:
            return f'The number {i} is not the smallest'
    else:
        return f'The number {i} is not in the list'

```


```python
get_large_small(10)
```




    'The number 10 is not the smallest'




```python

```


---
**Score: 5**
