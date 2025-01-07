---
title: Error-Enum
date: 2025-01-06
author: Your Name
cell_count: 7
score: 5
---

```python
from enum import Enum
```


```python
class ErrorCode(Enum):
    FILE_NOT_FOUND = 100
    ACCESS_DENIED = 101
    SERVER_ERROR = 500
```


```python
def handle_error(code):
    if code == ErrorCode.FILE_NOT_FOUND:
        return "File not found!"
    elif code == ErrorCode.ACCESS_DENIED:
        return "Access denied!"
    elif code == ErrorCode.SERVER_ERROR:
        return "Server error!"
    else:
        return "Unknown error"
```


```python
# Example usage
error_code = ErrorCode.ACCESS_DENIED
print(f"Error code {error_code.value}: {handle_error(error_code)}")
```

    Error code 101: Access denied!



```python
error_code = ErrorCode.FILE_NOT_FOUND
print(f"Error code {error_code.value}: {handle_error(error_code)}")
```

    Error code 100: File not found!



```python
error_code = ErrorCode.SERVER_ERROR
print(f"Error code {error_code.value}: {handle_error(error_code)}")
```

    Error code 500: Server error!



```python

```


---
**Score: 5**
