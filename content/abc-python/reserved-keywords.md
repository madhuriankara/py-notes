---
title: Reserved-Keywords
date: 2025-01-13
author: Your Name
cell_count: 32
score: 30
---

```python
# created on 20250113
```


```python
#https://www.scientecheasy.com/2022/09/reserved-keywords-in-python.html/
```


```python
import keyword
print(keyword.kwlist)

```

    ['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']



```python
#True and False
```


```python
print( 5 == 5 )
print( 10 > 9 )
print( True or False )
print( 9 <= 28 )

```

    True
    True
    True
    True



```python
print( True == 1 )
print( True + True + True)

```

    True
    3



```python
print(10 > 20)
print(50 <= 30)
print(False == 1)
print(False == 0)
print(False + False + 1) 

```

    False
    False
    False
    True
    1



```python
#None Keyword
```


```python
print(None == False)
print( None == 0 )
print( None == " " )

```

    False
    False
    False



```python
A = None
B = None
C = None
print( A == B )
print( B == C )
print( A == C )

```

    True
    True
    True



```python
print(True and True)
print(True and False and True)
print(True and 1)

```

    True
    False
    1



```python
print(True or True)
print(False or False or True)
print(True or False)
print(True or 1)

```

    True
    True
    True
    True



```python
num = [10, 20, 30, 40, 50]
print(50 in num)
print(15 in num)

```

    True
    False



```python
for i in 'keyword':
     print(i)

```

    k
    e
    y
    w
    o
    r
    d



```python
print( True == True )
print( False == True )
print( None == None )
print((2 + 4) == (3 * 2))

```

    True
    False
    True
    True



```python
#for loop
```


```python
for count in range(1, 4):
  print("Scientech Easy, Dhanbad")

```

    Scientech Easy, Dhanbad
    Scientech Easy, Dhanbad
    Scientech Easy, Dhanbad



```python
#while
```


```python
count = 0
while(count < 3):
    print("The current count is: ", count)
    count = count + 1
print("While loop ended!")

```

    The current count is:  0
    The current count is:  1
    The current count is:  2
    While loop ended!



```python
#break
```


```python
for i in range(1, 5):
    if i == 3:
        break
    print(i)

```

    1
    2



```python
#continue
```


```python
for i in range(1, 6):
    if i == 4:
       continue
    print(i)

```

    1
    2
    3
    5



```python
#Python Conditional keywords – if, else, and elif
```


```python
i = 10
if (i == 5):
    print ("Hello")
elif (i == 10):
    print ("Python keywords")
else:
    print ("Hello Python")

```

    Python keywords



```python
#def keyword
```


```python
# Declaring a user-defined function.
def func():
    print("Inside Function")
func()

```

    Inside Function



```python
#return keyword
```


```python
def func_return():
    x = 20
    return x

def func_no_return():
    y = 50
print(func_return())
print(func_no_return())

```

    20
    None



```python
#yield
```


```python
# Yield Keyword
def func():
    x = 0
    for i in range(5):
        x += i
        yield x
for i in func():
    print(i)

```

    0
    1
    3
    6
    10



```python

```


---
**Score: 30**
