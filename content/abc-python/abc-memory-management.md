---
title: Abc-Memory-Management
date: 2025-01-15
author: Your Name
cell_count: 8
score: 5
---

```python
#created on 20250115
```


```python
#https://www.scientecheasy.com/2022/09/memory-management-in-python.html/
```


```python
x = 10
print(id(x))

```

    4316160048



```python
x = 10
print(id(x))
y = 10
print(id(y))

```

    4316160048
    4316160048



```python
x = 10
print(id(x))

y = 10
print(id(y))

z = y
print(id(z))

```

    4316160048
    4316160048
    4316160048



```python
def func(x):
    value = (x + 5) * 10
    return value
x = 10
final_value = func(x)
print("Final value = ", final_value)

```

    Final value =  150



```python
def func(x):
    value = (x + 5) * 10
    return value

```


```python

```


---
**Score: 5**
