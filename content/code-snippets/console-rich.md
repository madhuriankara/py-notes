---
title: Console-Rich
date: 2025-01-15
author: Your Name
cell_count: 9
score: 5
---

```python
pip install rich

```

    Requirement already satisfied: rich in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (13.9.4)
    Requirement already satisfied: markdown-it-py>=2.2.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from rich) (3.0.0)
    Requirement already satisfied: pygments<3.0.0,>=2.13.0 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from rich) (2.18.0)
    Requirement already satisfied: mdurl~=0.1 in /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages (from markdown-it-py>=2.2.0->rich) (0.1.2)
    Note: you may need to restart the kernel to use updated packages.



```python
from rich.console import Console
from rich.text import Text
```


```python
# Create a console object
console = Console()
```


```python

```


```python
# Create rich text with styles
text = Text("Hello, world!", style="bold green on black")
text.append(" This is rich text!", style="underline yellow")
# Print the styled text to the console
console.print(text)
```


<pre style="white-space:pre;overflow-x:auto;line-height:normal;font-family:Menlo,'DejaVu Sans Mono',consolas,'Courier New',monospace"><span style="color: #008000; text-decoration-color: #008000; background-color: #000000; font-weight: bold">Hello, world!</span><span style="color: #808000; text-decoration-color: #808000; background-color: #000000; font-weight: bold; text-decoration: underline"> This is rich text!</span>
</pre>




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
