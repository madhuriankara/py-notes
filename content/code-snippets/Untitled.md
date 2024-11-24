---
title: Untitled
date: 2024-11-24
author: Your Name
cell_count: 3
score: 0
---

```python
import nmap                         # import nmap.py module
nm = nmap.PortScanner()             # instantiate nmap.PortScanner object
nm.scan('127.0.0.1', '22-443')      # scan host 127.0.0.1, ports from 22 to 443
nm.command_line()                   # get command line used for the scan : nmap -oX - -p 22-443 127.0.0.1
nm.scaninfo()                       # get nmap scan informations {'tcp': {'services': '22-443', 'method': 'connect'}}
```


    ---------------------------------------------------------------------------

    ModuleNotFoundError                       Traceback (most recent call last)

    Cell In[4], line 1
    ----> 1 import nmap                         # import nmap.py module
          2 nm = nmap.PortScanner()             # instantiate nmap.PortScanner object
          3 nm.scan('127.0.0.1', '22-443')      # scan host 127.0.0.1, ports from 22 to 443


    ModuleNotFoundError: No module named 'nmap'



```python

```


```python

```


---
**Score: 0**
