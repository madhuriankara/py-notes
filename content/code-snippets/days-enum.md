---
title: Days-Enum
date: 2024-11-27
author: Your Name
cell_count: 6
score: 5
---

```python
from enum import Enum, auto
```


```python
# Define an enumeration for days of the week
class Weekday(Enum):
    MONDAY = auto()
    TUESDAY = auto()
    WEDNESDAY = auto()
    THURSDAY = auto()
    FRIDAY = auto()
    SATURDAY = auto()
    SUNDAY = auto()
```


```python
 #Function to check if a given day is a weekday or weekend
def is_weekend(day):
    if day in (Weekday.SATURDAY, Weekday.SUNDAY):
        return True
    return False
```


```python
# Example usage
day = Weekday.THURSDAY

print(f"Day: {day.name}")
print(f"Is it a weekend? {'Yes' if is_weekend(day) else 'No'}")

```

    Day: THURSDAY
    Is it a weekend? No



```python
# Example usage
day = Weekday.SATURDAY

print(f"Day: {day.name}")
print(f"Is it a weekend? {'Yes' if is_weekend(day) else 'No'}")

```

    Day: SATURDAY
    Is it a weekend? Yes



```python

```


---
**Score: 5**
