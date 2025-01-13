---
title: Hexvalidator
date: 2025-01-13
author: Your Name
cell_count: 2
score: 0
---

```python
import webcolors

def is_valid_hex_color(color):
    try:
        webcolors.hex_to_rgb(color)
        return True
    except Exception as e :
        return False

# Examples
print(is_valid_hex_color("#FFF"))  # True
print(is_valid_hex_color("#123ABC"))  # True
print(is_valid_hex_color("#123ABCG"))  # False
```

    True
    True
    False



```python

```


---
**Score: 0**
