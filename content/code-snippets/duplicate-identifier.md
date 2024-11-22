---
title: Duplicate-Identifier
date: 2024-11-22
author: Your Name
cell_count: 5
score: 5
---

```python
import hashlib
import os

```


```python
def get_file_hash(file_path):
    """Generate a hash for the contents of a file."""
    hash_sha256 = hashlib.sha256()
    with open(file_path, 'rb') as f:
        while chunk := f.read(4096):
            hash_sha256.update(chunk)
    return hash_sha256.hexdigest()
```


```python
def find_duplicate_files(directory):
    seen = {}
    duplicates = []

    for root, _, files in os.walk(directory):
        for file in files:
            file_path = os.path.join(root, file)
            file_hash = get_file_hash(file_path)

            if file_hash in seen:
                duplicates.append(file_path)
            else:
                seen[file_hash] = file_path

    return duplicates


# Example usage: Replace with your directory path
directory_path = "/path/to/your/files"
duplicates = find_duplicate_files(directory_path)
print("Duplicate files:", duplicates)
```

    Duplicate files: []



```python

```


```python

```


---
**Score: 5**
