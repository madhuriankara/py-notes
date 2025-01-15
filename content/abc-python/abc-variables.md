---
title: Abc-Variables
date: 2025-01-15
author: Your Name
cell_count: 16
score: 15
---

```python
#created on 20250114
```


```python
#https://www.scientecheasy.com/2022/09/variables-in-python.html/
```


```python
#Variables in python
```


```python
num = 20 # an integer variable.

```


```python
num = 20
print(id(num))

```

    4304953712



```python
# Integer assignments.
x = 20 
y = 50
z = 100
# Print the values of variables on the console.
print(x)
print(y)
print(z)

```

    20
    50
    100



```python
phy = 89
chem = 86
maths = 90
# Adding the marks of three subjects.
marks_obtained = phy + chem + maths

# Calculating the percentage.
per = (marks_obtained * 100) / 300
# Displaying the marks obtained and percentage.
print("Marks obtained in three subjects: ", marks_obtained)
print("Percentage: ", per)

```

    Marks obtained in three subjects:  265
    Percentage:  88.33333333333333



```python
x = 80 # an integer assignment.
y = 99.99 # a floating point assignment.
name = 'Radhika' # a string assignment.
print(x); print(y); print(name);

```

    80
    99.99
    Radhika



```python
radius = 5
pi = 3.14
perimeter = 2 * pi * radius
area = 3.14 * radius * radius
print("Perimeter of the circle = ", perimeter)
print("Area of the circle = ", area)

```

    Perimeter of the circle =  31.400000000000002
    Area of the circle =  78.5



```python
# Assigning the new value to the same variable.
x = 10 
x = 'text'
print(x)
x = 25.50 
print(x)
x = True 
print(x)

```

    text
    25.5
    True



```python
x = y = z = 20
print(id(x))
print(id(y))
print(id(z))

```

    4304953712
    4304953712
    4304953712



```python
x, y, z = 20, 25.50, 'text'
print(id(x))
print(id(y))
print(id(z))

```

    4304953712
    4349586480
    4305008960



```python
fruit1, fruit2, fruit3 = "Banana", "Orange", "Mango"
print(fruit1)
print(fruit2)
print(fruit3)

```

    Banana
    Orange
    Mango



```python
num = 100
print(type(num))

```

    <class 'int'>



```python
num = 100.990
print(type(num))

```

    <class 'float'>



```python

```


---
**Score: 15**
