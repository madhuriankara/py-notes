---
title: Name-Generator
date: 2025-01-20
author: Your Name
cell_count: 5
score: 5
---

```python
import random
```


```python
def generate_random_name():
    first_names = ["Alice", "Bob", "Charlie", "Diana", "Eve", "Frank", "Grace", "Hank"]
    last_names = ["Smith", "Johnson", "Williams", "Brown", "Jones", "Garcia", "Miller", "Davis"]
    first_name = random.choice(first_names)
    last_name  = random.choice(last_names)
    full_name = f"{first_name}{last_name}"
    return full_name
```


```python
if __name__ == "__main__":
    print("Randomly Generated Names:")
    for _ in range(5):
        print(generate_random_name())
```

    Randomly Generated Names:
    GraceGarcia
    EveJones
    FrankBrown
    FrankJohnson
    DianaBrown



```python
if __name__ == "__main__":
    print("Randomly Generated Names:")
    for _ in range(5):
        print(generate_random_name())
```

    Randomly Generated Names:
    DianaMiller
    EveJones
    EveJohnson
    BobBrown
    DianaJohnson



```python

```


---
**Score: 5**
