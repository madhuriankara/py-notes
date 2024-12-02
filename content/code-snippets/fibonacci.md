---
title: Fibonacci
date: 2024-12-02
author: Your Name
cell_count: 9
score: 5
---

```python
def fibonacci(n):
    if n == 0: return 0
    elif n == 1: return 1
    else: return fibonacci(n-1)+fibonacci(n-2)
```


```python
## Example 1: Using looping technique
def fib(n):
    
    a, b = 1, 1

    for i in range(n-1):
        a, b = b, a+b
        print('b : ', b)

    return b
```


```python
## Example 1: Using looping technique
def fib_with_target(size, list):
    
    a, b = 0, 1

    for i in range(size):
        a, b = b, a+b
        print('Target#  '+str(i)+' - ', b)

        list.append(b)

    return b     
```


```python
def startpy():
    #a = fibonacci(10)
    #print(a)

    print(fib_with_target(23, []))
```


```python
if __name__ == '__main__':
    startpy()
```

    Target#  0 -  1
    Target#  1 -  2
    Target#  2 -  3
    Target#  3 -  5
    Target#  4 -  8
    Target#  5 -  13
    Target#  6 -  21
    Target#  7 -  34
    Target#  8 -  55
    Target#  9 -  89
    Target#  10 -  144
    Target#  11 -  233
    Target#  12 -  377
    Target#  13 -  610
    Target#  14 -  987
    Target#  15 -  1597
    Target#  16 -  2584
    Target#  17 -  4181
    Target#  18 -  6765
    Target#  19 -  10946
    Target#  20 -  17711
    Target#  21 -  28657
    Target#  22 -  46368
    46368



```python

```


```python

```


```python

```


```python

```


---
**Score: 5**
