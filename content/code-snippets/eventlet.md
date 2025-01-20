---
title: Eventlet
date: 2025-01-20
author: Your Name
cell_count: 7
score: 5
---

```python

```


```python
!pip install eventlet
```

    Requirement already satisfied: eventlet in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (0.38.0)
    Requirement already satisfied: dnspython>=1.15.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from eventlet) (2.7.0)
    Requirement already satisfied: greenlet>=1.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from eventlet) (3.1.1)



```python
import eventlet
import urllib.request  # Use the Python 3 urllib.request

def startpy():
    urls = [
        "https://www.youtube.com/",
        "https://www.google.com/",
    ]

    def fetch(url):
        # Use urllib from Python 3 to fetch data
        with urllib.request.urlopen(url) as response:
            return response.read()

    pool = eventlet.GreenPool()

    for body in pool.imap(fetch, urls):
        print("Got body:", len(body))

if __name__ == '__main__':
    startpy()

```

    Got body: 527625
    Got body: 19395



```python

```


```python


```


```python

```


```python

```


---
**Score: 5**
