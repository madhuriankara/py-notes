---
title: Abc-Pass-Statement
date: 2025-01-20
author: Your Name
cell_count: 9
score: 5
---

```python
#created on 20250120
```


```python
#https://www.scientecheasy.com/2022/11/python-pass-statement.html/
```


```python
x = 20
y = 30
if x > y:
    pass

```


```python
count = 0
while count <= 5:
    count = count + 1
    if count == 3:
        pass # nothing to be done on this line for output.
    print(count, end=' ')

```

    1 2 3 4 5 6 


```python
for x in range(2, 6):
    if x == 4:
        pass
    print(x, end=' ')

```

    2 3 4 5 


```python
for n in range(1, 11):
    if n % 2 == 0:
        pass 
    else:
        print(n, end=' ') 

```

    1 3 5 7 9 


```python
num = 6
while num > 0:
    if num == 3:
        pass
        print('Pass block executed')
    print('Current value: ',num)
    num = num - 1

```

    Current value:  6
    Current value:  5
    Current value:  4
    Pass block executed
    Current value:  3
    Current value:  2
    Current value:  1



```python


```


```python

```


---
**Score: 5**
