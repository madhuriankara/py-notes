---
title: Reserved-Keywords
date: 2025-01-15
author: Your Name
cell_count: 46
score: 45
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
#class Keyword
```


```python
class ClassExample:
    def func1(parameters):
        . . . .
    def func2(parameters):
        . . . .

```


      Cell In[36], line 3
        . . . .
        ^
    SyntaxError: invalid syntax




```python
#with Keyword
```


```python
with open('myfile.txt', 'w') as file:
    file.write('Scientech Easy!')

```


```python
#as Keyword
```


```python
import math as x
print(x.cos(0))

```

    1.0



```python
#lambda Keyword

```


```python
# Lambda keyword
cube = lambda x: x * x * x
print(cube(7))

```

    343



```python
#del Keyword
```


```python
my_var1 = 200
my_var2 = "Scientech Easy"

# check if my_var1 and my_var2 exists.
print(my_var1)
print(my_var2)

# delete both the variables.
del my_var1
del my_var2

# check if my_var1 and my_var2 exists
print(my_var1)
print(my_var2)

```

    200
    Scientech Easy



    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[44], line 13
         10 del my_var2
         12 # check if my_var1 and my_var2 exists
    ---> 13 print(my_var1)
         14 print(my_var2)


    NameError: name 'my_var1' is not defined



```python
#try, except, raise, and finally
```


```python
# initializing the value of variables.
x = 10
y = 0
# No exception raised in try block
try:
    z = x // y  # raises divide by zero exception.
    print(z)
# handles zero division exception
except ZeroDivisionError:
    print("Cannot divide by zero")

finally:
    # this block always gets executed regardless of exception produced.
    print('finally block always gets executed')

```

    Cannot divide by zero
    finally block always gets executed



```python
#assert Keyword
```


```python
x = 10
assert x >= 10
assert x < 10
```


    ---------------------------------------------------------------------------

    AssertionError                            Traceback (most recent call last)

    Cell In[49], line 3
          1 x = 10
          2 assert x >= 10
    ----> 3 assert x < 10


    AssertionError: 



```python

```


---
**Score: 45**
