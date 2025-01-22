---
title: Abc-Break
date: 2025-01-22
author: Your Name
cell_count: 6
score: 5
---

```python
#created on 20250120
```


```python
#https://www.scientecheasy.com/2022/11/break-statement-in-python.html/
```


```python
for x in range(1, 11):
    if x == 5:
        break 
    print("X = ",x)

```

    X =  1
    X =  2
    X =  3
    X =  4



```python
for letter in 'Python':
    if letter == 't':
        break
    print('Current letter is ',letter)

```

    Current letter is  P
    Current letter is  y



```python
num = int(input('Enter a number: '))
num_list = [20, 40, 60, 80, 100, 120]
for n in num_list:
    if n == num:
        print('Entered number found in the list.')
        break
else:
    print('Entered number not found in the list.')

```

    Enter a number:  79


    Entered number not found in the list.



```python

```


---
**Score: 5**
