---
title: Abc-Datatypes
date: 2025-01-22
author: Your Name
cell_count: 27
score: 25
---

```python
#created on 20250115
```


```python
#https://www.scientecheasy.com/2022/09/data-types-in-python.html/
```


```python
#datatypes
```


```python
my_var = "Hi Friends!" 
my_var = 25
my_var = True 

```


```python
#int datatype
```


```python
num1 = 10
num2 = 20
num3 = 30
print(num1)
print(num2)
print(num3)

```

    10
    20
    30



```python
num1 = 100
num2 = 200
result = num1 + num2
print(result)

```

    300



```python
#Float Data type
```


```python
num1 = 10.555
num2 = 20.99
result = num1 + num2
print(result)

```

    31.544999999999998



```python
num1 = 1.20E5
num2 = 2.30E5
result = num1 + num2
print(result)

```

    350000.0



```python
#Boolean datatype
```


```python
a = (10 >= 4)
b = (25 == 5 * 5)
c = (18 != 2 * 9)
# Use the print function to see values stored in each variable.
print(a, b, c)

```

    True True False



```python
a = True
b = True + 5 
c = False * False
print(a, b, c)
print(type(a))

```

    True 6 0
    <class 'bool'>



```python
a = None
print(a)
print(type(a))

```

    None
    <class 'NoneType'>



```python
#String Data type in Python
```


```python
str1 = "Hello Python"
str2 = 'Happy birthday to you'
print(str1)
print(str2)
print(type(str1))

```

    Hello Python
    Happy birthday to you
    <class 'str'>



```python
str = """Welcome to Scientech Easy,
           Dhanbad, Jharkhand, India."""

```


```python
#List Data type
```


```python
list = [10, 20.50, "Python", True]
print(list)
print(type(list))

```

    [10, 20.5, 'Python', True]
    <class 'list'>



```python
num_list = [10, 20, 30, 40]
print(num_list)
num_list[2] = 50 # updating element.
print(num_list)

```

    [10, 20, 30, 40]
    [10, 20, 50, 40]



```python
#Tuple Data type
```


```python
t = (10, 20, "Python", 2 + 10j)
print(t)
print(type(t))

```

    (10, 20, 'Python', (2+10j))
    <class 'tuple'>



```python
#Set Data type
```


```python
s = {1, 2, 'Hello', 4 + 50j}
print(s)
print(type(s))

```

    {1, 2, (4+50j), 'Hello'}
    <class 'set'>



```python
#Dictionary Data type
```


```python
dict = {1 : 'Orange',
        2 : 'Apple',
        3 : 'Banana'}
print(dict)
print(type(dict))

```

    {1: 'Orange', 2: 'Apple', 3: 'Banana'}
    <class 'dict'>



```python

```


---
**Score: 25**
