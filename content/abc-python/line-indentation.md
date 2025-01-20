---
title: Line-Indentation
date: 2025-01-20
author: Your Name
cell_count: 15
score: 15
---

```python
# created on 20250113
```


```python
# https://www.scientecheasy.com/2022/09/indentation-in-python.html/
```


```python
# line indentation
```


```python
def display():
    var = "Scientech Easy"
    print(var)
display()
```

    Scientech Easy



```python
## Declare a user-defined function with parameter.
```


```python
def display(parameter):
    var = "Hello"
    print(var)
    print(var, parameter)
display("Python")
```

    Hello
    Hello Python



```python
#line indentation
```


```python
name = 'Ivaan'
if name == 'Ivaan':
    print('WelCome Ivaan..')
    print('How are you, today?')
else:
    print('Dude! whoever are you ')
    print('Why are you here?')

print('I am fine, thank you!')
print('Have a nice day!')
    
```

    WelCome Ivaan..
    How are you, today?
    I am fine, thank you!
    Have a nice day!



```python
#An example in which we will use two different blocks with two different sets of indentation.
```


```python
def school(parameter):
  print(parameter) 

def city(parameter):
    print(parameter)

# Calling methods.
school('RSVM')
city('Dhanbad')
```

    RSVM
    Dhanbad



```python
#Mismatch Indentation
```


```python
a = 10
b = 20
c = 30
if(b > a):
  print("b is greater than a")
    print("b is greater than a but less than c")
```


      Cell In[12], line 6
        print("b is greater than a but less than c")
        ^
    IndentationError: unexpected indent




```python
a = 10
b = 20
c = 30
if(b > a):
  print("b is greater than a")
  print("b is greater than a but less than c")
```

    b is greater than a
    b is greater than a but less than c



```python
def display(): 
    name = 'John'
    print(name)
display()
```

    John



```python

```


---
**Score: 15**
