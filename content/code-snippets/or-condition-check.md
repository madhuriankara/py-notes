---
title: Or-Condition-Check
date: 2025-01-13
author: Your Name
cell_count: 2
score: 0
---

```python
def get_master_data(namespace, 
                    entity,
                    filter_in = None,
                    return_ = None,
                    return_expect = None):

    param_available = False

    
    if(filter_in or return_ or return_expect):
        param_available = True

    print(f'param available : {param_available}')


def append_test():

    x = "one"

    x += " two"

    print(x)



def startpy():
    
    # get_master_data('ns', 'en')
    # get_master_data('ns', 'en', filter_in='a>4')

    append_test()


if __name__ == '__main__':
    startpy()
```

    one two



```python

```


---
**Score: 0**
