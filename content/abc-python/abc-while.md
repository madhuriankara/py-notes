---
title: Abc-While
date: 2025-01-22
author: Your Name
cell_count: 8
score: 5
---

```python
#created on 20250120
```


```python
#https://www.scientecheasy.com/2022/10/while-loop-in-python.html/
```


```python
i = 1 # Initialization.
while i <= 5:
    print('Current value of i is ',i)
    i = i + 1 # Increment by 1.

```

    Current value of i is  1
    Current value of i is  2
    Current value of i is  3
    Current value of i is  4
    Current value of i is  5



```python
i = 0 
name = input('Enter your name: ')
while i < 5:
    print(name)
    i = i + 1 # Increment by 1.

```

    Enter your name:  rita


    rita
    rita
    rita
    rita
    rita



```python
i = 5 # Initialization.
while i >= 1:
    print(i)
    i = i - 1 # decrement by 1.
print('Loop finished')
```

    5
    4
    3
    2
    1
    Loop finished



```python
# Program to display the average of n natural numbers.
num = int(input('Enter a number up to which you want to calculate average: '))
i = 0
sum = 0
count = 0 # Initialization.
while i < num:
    i = i + 1 # Increment by 1.
    sum = sum + i
    count = count + 1
average = sum / count
print('Average of', num,'natural numbers = ', average)

```

    Enter a number up to which you want to calculate average:  7


    Average of 7 natural numbers =  4.0



```python
# Program to display the sum of first 10 natural numbers.
sum = 0
count = 0 # Initialization.
while count <= 10:
    sum = sum + count
    count = count + 1
print('Sum of 10 natural numbers = ', sum)

```

    Sum of 10 natural numbers =  55



```python

```


---
**Score: 5**
