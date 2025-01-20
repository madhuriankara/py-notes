---
title: Abc-Local-Gloabal
date: 2025-01-20
author: Your Name
cell_count: 10
score: 10
---

```python
#created on 20250115
```


```python
#https://www.scientecheasy.com/2022/09/global-and-local-variables-in-python.html/
```


```python
#Global and Local Variables in Python
```


```python
x = 20 # a global variable.
def my_function():
    print("Inside function: ", x)
my_function()
print("Outside function: ", x)

```

    Inside function:  20
    Outside function:  20



```python
x = 20
def my_function():
    x = 20 * 30 
    print("Inside function: ", x)
my_function()
print("Outside function: ", x)

```

    Inside function:  600
    Outside function:  20



```python
name = 'John' 
def my_function1():
    global name
    name = 'Bob' 
    print("Inside function: ", name)
def my_function2():
    print("Inside another function: ", name)

my_function1()
my_function2()

# Accessing the global variable from outside the functions.
print("Outside function: ", name)

```

    Inside function:  Bob
    Inside another function:  Bob
    Outside function:  Bob



```python
city = 'New York' 
def my_function1():
    global city
    city = 'Dhanbad'
    print("Inside my_function1: ", city)
def my_function2():
    global city
    city = 'Sydney'
    print("Inside my_function2: ",city)
my_function1()
my_function2()
print("Outside function: ", city)

```

    Inside my_function1:  Dhanbad
    Inside my_function2:  Sydney
    Outside function:  Sydney



```python
message1 = "This is a global variable, and we can access it anywhere in the program."
def display():
    message2 = "This is a local variable, and we can access it only inside the function body."
    print(message2) 

print(message1); 
display() 


```

    This is a global variable, and we can access it anywhere in the program.
    This is a local variable, and we can access it only inside the function body.



```python
student1 = "John"
student2 = "Larry"

def showMe():
    student2 = "Harry" 
    student3 = "Deep"
    print(student2, " ",student3)

showMe(); # calling function.
print(student1, " ", student2)

```

    Harry   Deep
    John   Larry



```python

```


---
**Score: 10**
