---
title: Abc-Literals
date: 2025-01-15
author: Your Name
cell_count: 30
score: 30
---

```python
#created on 20250113
```


```python
#https://www.scientecheasy.com/2022/09/literals-in-python.html/
```


```python
#Literals
```


```python
#single-line literal
```


```python
single_line_string = ‘Scientech Easy’
```


```python
#Multi-line String
```


```python
multi_line_string = 'Welcome \
to \
Scientech Easy'
print(multi_line_string)

```

    Welcome to Scientech Easy



```python
#We can also create a multi-line string literal using triple quotation marks.
```


```python
multi_line_string = '''Welcome \
to \
Scientech Easy, \
Dhanbad'''
print(multi_line_string)

```

    Welcome to Scientech Easy, Dhanbad



```python
#Numeric literal 
```


```python
x = 50 # Decimal integer
y = 0o62 # Octal integer
z = 0x32 # Hexadecimal integer

print("Decimal literal representation: ", x)
print("Octal literal representation: ", y)
print("Hexadecimal representation: ", z)

```

    Decimal literal representation:  50
    Octal literal representation:  50
    Hexadecimal representation:  50



```python
#floating-point
```


```python
x = 75e-2
y = 0.75
print(x)
print(y)

```

    0.75
    0.75



```python
#Complex literal
```


```python
# complex literal
a = 5 + 10j
b = 2j
print(a)
print(b)

```

    (5+10j)
    2j



```python
#Boolean literals
```


```python
# boolean literals
a = (9 == 9)
b = (5 == False)
c = True + 5
d = False + 5 

print("a is ", a)
print("b is ", b)
print("c is ", c)
print("d is ", d)

```

    a is  True
    b is  False
    c is  6
    d is  5



```python
#Special literals
#Python language contains only one special literal, i.e., None
```


```python
# Special literals
a = None
print(a) 

```

    None



```python
#List literals
```


```python
# List literals
address = ['Scientech Easy', 'Joraphatak Road', 'Dhanbad']
print(address)

```

    ['Scientech Easy', 'Joraphatak Road', 'Dhanbad']



```python
num = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print(num)

```

    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]



```python
#Dictionary Literals
```


```python
# Dictionary literals
fruits_dict = {'a': 'apple',
               'o': 'orange',
               'b': 'banana'}
print(fruits_dict)

```

    {'a': 'apple', 'o': 'orange', 'b': 'banana'}



```python
#Tuple Literals
```


```python
# tuple literals
even_numbers = (2, 4, 6, 8, 10, 12)
vowels = ('a','e','i','o','u')
direction = ('North', 'South', 'East', 'West')

print(even_numbers)
print(vowels)
print(direction)

```

    (2, 4, 6, 8, 10, 12)
    ('a', 'e', 'i', 'o', 'u')
    ('North', 'South', 'East', 'West')



```python
#Set Literals
#Set literals in Python are a well-defined collection of unordered data that cannot be changed.
```


```python
# Set literals
fruits = {'Apple', 'Mango', 'Banana', 'Orange', 'Grape'}
print(fruits)

```

    {'Apple', 'Grape', 'Mango', 'Orange', 'Banana'}



```python
# Set literals
fruits = {'Apple', 'Mango', 'Banana', 'Orange', 'Grape'}
print(fruits)

```

    {'Apple', 'Grape', 'Mango', 'Orange', 'Banana'}



```python

```


---
**Score: 30**
