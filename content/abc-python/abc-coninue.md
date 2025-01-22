---
title: Abc-Coninue
date: 2025-01-22
author: Your Name
cell_count: 7
score: 5
---

```python
#created on 20150120
```


```python
#https://www.scientecheasy.com/2022/11/python-continue.html/
```


```python
for letter in 'Technology':
    if letter == 'n':
        print('Skipping the loop at', letter)
        continue
    print(letter)
```

    T
    e
    c
    h
    Skipping the loop at n
    o
    l
    o
    g
    y



```python
x = 1 # Initialization.
while x <= 6:
    if x == 3:
        x = x + 1
        continue
    print(x)
    x = x + 1

```

    1
    2
    4
    5
    6



```python
for x in range(1, 4):
     for y in range(1, 4):
       if x == 2 and y == 3:
           continue 
       print(x,y)

```

    1 1
    1 2
    1 3
    2 1
    2 2
    3 1
    3 2
    3 3



```python
for x in range(1, 7):
    if x < 2:
        continue
    print(x)
    if x < 4:
        continue
    print(10 * x)

```

    2
    3
    4
    40
    5
    50
    6
    60



```python

```


---
**Score: 5**
