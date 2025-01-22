---
title: Signal-Enum
date: 2025-01-22
author: Your Name
cell_count: 7
score: 5
---

```python
from enum import Enum
```


```python
class TrafficLight(Enum):
    RED = 1
    YELLOW = 2
    GREEN = 3
```


```python
def traffic_light_action(light):
    if light == TrafficLight.RED:
        return "Stop"
    elif light == TrafficLight.YELLOW:
        return "Slow down"
    elif light == TrafficLight.GREEN:
        return "Go"
    else:
        return "Invalid light"
```


```python
# Example usage
light = TrafficLight.RED
print(f"Traffic light is {light.name}: {traffic_light_action(light)}")
```

    Traffic light is RED: Stop



```python
light = TrafficLight.YELLOW
print(f"Traffic light is {light.name}: {traffic_light_action(light)}")
```

    Traffic light is YELLOW: Slow down



```python
light = TrafficLight.GREEN
print(f"Traffic light is {light.name}: {traffic_light_action(light)}")
```

    Traffic light is GREEN: Go



```python

```


---
**Score: 5**
