---
title: 1 Address
date: 2024-11-22
author: Your Name
cell_count: 12
score: 10
---

```python
from faker import Faker

fake = Faker()
```


```python
!pip install faker

```

    Collecting faker
      Downloading Faker-33.0.0-py3-none-any.whl.metadata (15 kB)
    Requirement already satisfied: python-dateutil>=2.4 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from faker) (2.9.0.post0)
    Requirement already satisfied: typing-extensions in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from faker) (4.12.2)
    Requirement already satisfied: six>=1.5 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from python-dateutil>=2.4->faker) (1.16.0)
    Downloading Faker-33.0.0-py3-none-any.whl (1.9 MB)
    [2K   [38;2;114;156;31m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m1.9/1.9 MB[0m [31m14.4 MB/s[0m eta [36m0:00:00[0m
    [?25hInstalling collected packages: faker
    Successfully installed faker-33.0.0



```python
for _ in range(5):
    SUITE_NO = f'{fake.random_int(1,99)}/{fake.random_int(1,70)}'
```


```python
    STREET_NAME = fake.street_name()
```


```python
print(f'{SUITE_NO} {STREET_NAME}')
```

    80/63 Kim Pike



```python
print(f'{SUITE_NO} {STREET_NAME}')
```

    80/63 Kim Pike



```python
for _ in range(5):
    SUITE_NO = f'{fake.random_int(1,60)}/{fake.random_int(1,70)}'
```


```python
STREET_NAME = fake.street_name()
```


```python
print(f'{SUITE_NO} {STREET_NAME}')
```

    28/68 Sloan Hill



```python
STREET_NAME = fake.street_name()
```


```python
print(f'{SUITE_NO} {STREET_NAME}')
```

    28/68 Lin Isle



```python

```


---
**Score: 10**
