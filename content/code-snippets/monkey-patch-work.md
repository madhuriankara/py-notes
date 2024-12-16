---
title: Monkey-Patch-Work
date: 2024-12-15
author: Your Name
cell_count: 6
score: 5
---

```python

```


```python
!pip install gevent
```

    Requirement already satisfied: gevent in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (24.11.1)
    Requirement already satisfied: zope.event in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from gevent) (5.0)
    Requirement already satisfied: zope.interface in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from gevent) (7.1.1)
    Requirement already satisfied: greenlet>=3.1.1 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from gevent) (3.1.1)
    Requirement already satisfied: setuptools in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from zope.event->gevent) (75.1.0)



```python


from gevent import monkey, sleep
monkey.patch_all()

import threading 


class ExampleThread(threading.Thread):
    def run(self):
        for i in range(10):
            print('working')
            sleep()

if __name__ == '__main__':
    worker = ExampleThread()
    worker.start()
    print('this will be printed after the first call to sleep')
```

    working
    this will be printed after the first call to sleep
    working
    working
    working
    working
    working
    working
    working
    working
    working



```python

```


```python

```


```python

```


---
**Score: 5**
