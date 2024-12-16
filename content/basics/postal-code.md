---
title: Postal-Code
date: 2024-12-15
author: Your Name
cell_count: 4
score: 0
---

```python
def postal_code(number):
    try:
        Zipcode_number = int(number)
        print("This is an Indian code")
    except ValueError as e:
        print("This is an Canadian postalcode")
        

        
```


```python
postal_code("M1E5E6")
```

    This is an Canadian postalcode



```python
postal_code("1234567")
```

    This is an Indian code



```python

```


---
**Score: 0**
