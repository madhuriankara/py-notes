---
title: Abc-If-
date: 2025-01-22
author: Your Name
cell_count: 11
score: 10
---

```python
#created on 20250121
```


```python
if(True): # Here, we have used a boolean value True to check whether the condition is true or not.
    print("Code to be executed") # It will print statement. 

if(False): 
    print("Code not to be executed") # It will not print statement.
```

    Code to be executed



```python
x = 1
if x > 0:
    print(x, " is a positive number")

x = 10
if(x): # same as: if(x != 0)
    print(x, " is a nonzero number");

x, y = 10, 10
if(x == y):
    print("x and y are equal number")

x, y = 5, 10
if x < y:
    print("x is less than y")

x = True
if(x): # Here, we have used a boolean value to check whether the condition is true or not.
    print("You are eligible to cast vote")

```

    1  is a positive number
    10  is a nonzero number
    x and y are equal number
    x is less than y
    You are eligible to cast vote



```python
radius = 2.5
pi = 3.14
if radius >= 0:
    area = radius * radius * pi
    print("Area of circle: ", area)

```

    Area of circle:  19.625



```python
# Prompt the user to enter a number.
num = int(input("Enter a number that you want to check it is divisible by 2 or not: "))
if num % 2 == 0:
    print(num, " is divisible by 2.")
if num % 2 != 0:
    print(num, " is not divisible by 2.")

```

    Enter a number that you want to check it is divisible by 2 or not:  9


    9  is not divisible by 2.



```python
# Prompt the user to enter your age.
age = int(input("Enter your age to check you are eligible to cast a vote or not: "))
if age >= 18:
    print("You are eligible to cast a vote.")

if age < 18:
    print("You are not eligible to cast a vote")

```

    Enter your age to check you are eligible to cast a vote or not:  30


    You are eligible to cast a vote.



```python
# Prompt the user to enter marks of three subjects.
phy = int(input("Enter your physics marks: "))
chem = int(input("Enter your chemistry marks: "))
maths = int(input("Enter your math marks: "))
totalMarks = phy + chem + maths

myPer = totalMarks / 3
print("Total marks obtained: ", totalMarks)
print("Your percentage: ", myPer)

if(myPer >= 90.0): 
    print("Grade A")
if(myPer < 90.0): 
    print("Grade B")

```

    Enter your physics marks:  99
    Enter your chemistry marks:  99
    Enter your math marks:  99


    Total marks obtained:  297
    Your percentage:  99.0
    Grade A



```python
# Read the number from the user to check even or odd.
num = int(input("Enter a number: "))
if num % 2 == 0:
    print(num, 'is an even number')
if num % 2 != 0:
    print(num, 'is a odd number')

```

    Enter a number:  9


    9 is a odd number



```python
x, y, z = 20, 40, 50
if((y > x) and (y < z)): # True 
     print("y is greater than x but smaller than z") 
if((x > y) and (y < z)): # False
     print("z is greater than x, y")
if(y % x == 0 and x != 0): # True
     print("y is divisible by x")

```

    y is greater than x but smaller than z
    y is divisible by x



```python
x, y, z = 2, 1, 4
if(value := x > y or y < z): 
    print(value) 
if(value := x > y or y > z):
    print(value)

if(value := x < y or y < z):
    print(value)
if(value := x < y or y > z):
    print(value)

```

    True
    True
    True



```python

```


---
**Score: 10**
