---
title: Question3
date: 2024-12-02
author: Your Name
cell_count: 5
score: 5
---

def find_common_elements(list1, list2):
    """
    Given two lists, find the common elements between them.

    Args:
    list1: First list of elements
    list2: Second list of elements

    Returns:
    List of common elements between list1 and list2
    """

    # Initialize an empty list to store common elements
    common_elements = []

    # pass

# Sample test cases
# print(find_common_elements([1, 2, 3, 4, 5], [4, 5, 6, 7, 8])) # Output should be [4, 5]
# print(find_common_elements(['a', 'b', 'c'], ['b', 'c', 'd'])) # Output should be ['b', 'c']
```


```python
def find_common_elements(list1, list2):
    common_elements =[]
    list1: [1,2,3,4,5]
    list2: [4,5,6,7,8]
    for i in list1:
        for i in list2:
            common_elements.append(i)
            print f'{common_elemets}'

```


      Cell In[13], line 8
        print f'{common_elemets}'
        ^
    SyntaxError: Missing parentheses in call to 'print'. Did you mean print(...)?




```python
print(find_common_elements([1, 2, 3, 4, 5], [4, 5, 6, 7, 8])) # Output should be [4, 5]

```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[14], line 1
    ----> 1 print(find_common_elements([1, 2, 3, 4, 5], [4, 5, 6, 7, 8])) # Output should be [4, 5]


    Cell In[11], line 8, in find_common_elements(list1, list2)
          6 for i in list2:
          7     common_elements.append(i)
    ----> 8     print(f'{common_elemets}')


    NameError: name 'common_elemets' is not defined



```python

```


```python

```


---
**Score: 5**
