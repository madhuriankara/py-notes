---
title: Regex
date: 2024-12-15
author: Your Name
cell_count: 7
score: 5
---

```python
import re
```


```python
text = "My email addresses are madhuri@gmail.com, ankaraboyina@yahoo.com, and keerthi@hotmail.com."

```


```python
email_pattern = r"[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}"
```


```python
emails = re.findall(email_pattern, text)
print("Found email addresses:", emails)

```

    Found email addresses: ['madhuri@gmail.com', 'ankaraboyina@yahoo.com', 'keerthi@hotmail.com']



```python
text_with_placeholder = re.sub(email_pattern, "[email protected]", text)
print("\nText with replaced email addresses:", text_with_placeholder)

```

    
    Text with replaced email addresses: My email addresses are [email protected], [email protected], and [email protected].



```python
email_check = re.search(email_pattern, text)
if email_check:
    print("\nValid email address found:", email_check.group())
else:
    print("\nNo valid email address found.")
```

    
    Valid email address found: madhuri@gmail.com



```python

```


---
**Score: 5**
