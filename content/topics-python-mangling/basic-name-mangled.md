---
title: Basic-Name-Mangled
date: 2025-01-20
author: Your Name
cell_count: 14
score: 10
---

```python
#created on 20250115
```


```python
 #Basic Name-Mangled Method
```


```python
class MyClass:
    def __hidden_method(self):
        print("This is a hidden method!")

    def call_hidden(self):
        self.__hidden_method()

obj = MyClass()
obj.call_hidden()  

obj._MyClass__hidden_method()  

```

    This is a hidden method!
    This is a hidden method!



```python
#dunder method
```


```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __str__(self):
        return f"{self.name}, {self.age} years old"

person = Person("Alice", 30)
print(person)  # Output: Alice, 30 years old

```

    Alice, 30 years old



```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __repr__(self):
        return f"Person(name='{self.name}', age={self.age})"

p = Person("Alice", 30)
print(repr(p))  # Output: Person(name='Alice', age=30)

```

    Person(name='Alice', age=30)



```python
#self vs class
```


```python
class MyClass:
    def __init__(self, value):
        self.value = value 

    def display_value(self):
        print(self.value)  

obj1 = MyClass(10)
obj2 = MyClass(20)

obj1.display_value()  # Output: 10
obj2.display_value()  # Output: 20

```

    10
    20



```python
class Dog:
    def __init__(self, name):
        self.name = name  # 'self.name' belongs to the specific dog

    def speak(self):
        print(f"{self.name} says woof!")

dog1 = Dog("Buddy")  
dog2 = Dog("Charlie")  

dog1.speak() 
dog2.speak() 

```

    Buddy says woof!
    Charlie says woof!



```python
class Car:
    def __init__(self, brand, color):
        self.brand = brand  
        self.color = color  

    def drive(self):
        print(f"The {self.color} {self.brand} is driving.")


car1 = Car("Toyota", "Red")
car2 = Car("Honda", "Blue")

print(car1.brand)  
print(car2.color)  

car1.drive()  
car2.drive()  

```

    Toyota
    Blue
    The Red Toyota is driving.
    The Blue Honda is driving.



```python
#__str__
```


```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __str__(self):
        return f"{self.name}, {self.age} years old"

p = Person("Alice", 30)
print(p)  

```

    Alice, 30 years old



```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __str__(self):
        return f"{self.name}, {self.age} years old"  # User-friendly

    def __repr__(self):
        return f"Person(name='{self.name}', age={self.age})"  # Developer-friendly

p = Person("Charlie", 40)
print(str(p))   
print(repr(p))  
```

    Charlie, 40 years old
    Person(name='Charlie', age=40)



```python

```


---
**Score: 10**
