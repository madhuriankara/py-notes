---
title: Name-Mangled
date: 2025-01-20
author: Your Name
cell_count: 6
score: 5
---

```python
#created on 20250116
```


```python
#Name Mangling in a Base and Subclass
```


```python
class Base:
    def __init__(self):
        self.__private_var = "Base private variable"
    
    def show_private_var(self):
        return self.__private_var

class Sub(Base):
    def __init__(self):
        super().__init__()
        self.__private_var = "Subclass private variable"

base_obj = Base()
print(base_obj.show_private_var())  

sub_obj = Sub()
print(sub_obj.show_private_var())  
print(sub_obj._Sub__private_var)    
```

    Base private variable
    Base private variable
    Subclass private variable



```python
#Accessing Mangled Attributes
```


```python
class Example:
    def __init__(self):
        self.__hidden = "Hidden Value"

    def get_hidden(self):
        return self.__hidden

obj = Example()
print(obj.get_hidden())        
print(obj._Example__hidden)    

```

    Hidden Value
    Hidden Value



```python

```


---
**Score: 5**
