---
title: Question8
date: 2024-12-13
author: Your Name
cell_count: 3
score: 0
---

```python
def reverse_words(sentence):
    """
    Given a sentence, reverse the order of words in it.

    Args:
    sentence: A string representing the input sentence.

    Returns:
    A string with words in reversed order.
    """

    # Split the sentence into words
    words = sentence.split()

    # do your code

    return reversed_sentence

# Test cases
# print(reverse_words("Hello World"))  # Output: "World Hello"
# print(reverse_words("Python is awesome"))  # Output: "awesome is Python"
# print(reverse_words("Coding test in Python"))  # Output: "Python in test Coding"
```


```python
def reverse_words(sentence):
    words = sentence.split()
    return " ".join(words[::-1])
    
        
        
print(reverse_words("Hello World"))  # Output: "World Hello"
print(reverse_words("Python is awesome"))  # Output: "awesome is Python"
print(reverse_words("Coding test in Python"))  # Output: "Python in test Coding"
    
    
```

    World Hello
    awesome is Python
    Python in test Coding



```python

```


---
**Score: 0**
