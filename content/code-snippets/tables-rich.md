---
title: Tables-Rich
date: 2024-11-28
author: Your Name
cell_count: 8
score: 5
---

```python
from rich.console import Console
from rich.table import Table
```


```python
# Create a table object
table = Table(title="Example Table")
```


```python
# Add columns to the table
table.add_column("ID", justify="right", style="cyan", no_wrap=True)
table.add_column("Name", style="magenta")
table.add_column("Age", justify="center", style="green")
```


```python
# Add rows to the table
table.add_row("1", "Alice", "24")
table.add_row("2", "Bob", "30")
table.add_row("3", "Charlie", "22")
```


```python
# Create a console object
console = Console()

# Print the table to the console
console.print(table)
```


<pre style="white-space:pre;overflow-x:auto;line-height:normal;font-family:Menlo,'DejaVu Sans Mono',consolas,'Courier New',monospace"><span style="font-style: italic">    Example Table     </span>
┏━━━━┳━━━━━━━━━┳━━━━━┓
┃<span style="font-weight: bold"> ID </span>┃<span style="font-weight: bold"> Name    </span>┃<span style="font-weight: bold"> Age </span>┃
┡━━━━╇━━━━━━━━━╇━━━━━┩
│<span style="color: #008080; text-decoration-color: #008080">  1 </span>│<span style="color: #800080; text-decoration-color: #800080"> Alice   </span>│<span style="color: #008000; text-decoration-color: #008000"> 24  </span>│
│<span style="color: #008080; text-decoration-color: #008080">  2 </span>│<span style="color: #800080; text-decoration-color: #800080"> Bob     </span>│<span style="color: #008000; text-decoration-color: #008000"> 30  </span>│
│<span style="color: #008080; text-decoration-color: #008080">  3 </span>│<span style="color: #800080; text-decoration-color: #800080"> Charlie </span>│<span style="color: #008000; text-decoration-color: #008000"> 22  </span>│
└────┴─────────┴─────┘
</pre>




```python
# Add rows to the table
table.add_row("1", "Madhuri", "36")
table.add_row("2", "Keerthi", "33")
table.add_row("3", "Anu", "32")
```


```python
console.print(table)
```


<pre style="white-space:pre;overflow-x:auto;line-height:normal;font-family:Menlo,'DejaVu Sans Mono',consolas,'Courier New',monospace"><span style="font-style: italic">    Example Table     </span>
┏━━━━┳━━━━━━━━━┳━━━━━┓
┃<span style="font-weight: bold"> ID </span>┃<span style="font-weight: bold"> Name    </span>┃<span style="font-weight: bold"> Age </span>┃
┡━━━━╇━━━━━━━━━╇━━━━━┩
│<span style="color: #008080; text-decoration-color: #008080">  1 </span>│<span style="color: #800080; text-decoration-color: #800080"> Alice   </span>│<span style="color: #008000; text-decoration-color: #008000"> 24  </span>│
│<span style="color: #008080; text-decoration-color: #008080">  2 </span>│<span style="color: #800080; text-decoration-color: #800080"> Bob     </span>│<span style="color: #008000; text-decoration-color: #008000"> 30  </span>│
│<span style="color: #008080; text-decoration-color: #008080">  3 </span>│<span style="color: #800080; text-decoration-color: #800080"> Charlie </span>│<span style="color: #008000; text-decoration-color: #008000"> 22  </span>│
│<span style="color: #008080; text-decoration-color: #008080">  1 </span>│<span style="color: #800080; text-decoration-color: #800080"> Madhuri </span>│<span style="color: #008000; text-decoration-color: #008000"> 36  </span>│
│<span style="color: #008080; text-decoration-color: #008080">  2 </span>│<span style="color: #800080; text-decoration-color: #800080"> Keerthi </span>│<span style="color: #008000; text-decoration-color: #008000"> 33  </span>│
│<span style="color: #008080; text-decoration-color: #008080">  3 </span>│<span style="color: #800080; text-decoration-color: #800080"> Anu     </span>│<span style="color: #008000; text-decoration-color: #008000"> 32  </span>│
└────┴─────────┴─────┘
</pre>




```python

```


---
**Score: 5**
