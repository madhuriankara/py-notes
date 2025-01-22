---
title: %%Time
date: 2025-01-22
author: Your Name
cell_count: 3
score: 0
---

```python
%%time
# Generate squares of numbers from 1 to 1 million using a loop
squares = []
for i in range(1, 1_000_001):
    squares.append(i**2)
```

    CPU times: user 87 ms, sys: 7.4 ms, total: 94.4 ms
    Wall time: 95.2 ms



```python
%%timeit
# Generate squares of numbers from 1 to 1 million using a list comprehension
squares = [i**2 for i in range(1, 1_000_001)]

```

    39.6 ms ± 431 μs per loop (mean ± std. dev. of 7 runs, 10 loops each)



```python

```


---
**Score: 0**
