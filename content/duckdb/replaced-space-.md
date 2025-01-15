---
title: Replaced-Space-
date: 2025-01-15
author: Your Name
cell_count: 3
score: 0
---

```python
import pandas as pd

# Load the CSV file
file_path = 'onlinefoods.csv'
data = pd.read_csv(file_path)

# Replace spaces in column names with dashes
data.columns = data.columns.str.replace(' ', '-')
data['Monthly Income'] = data['Monthly-Income'].replace('No Income', '--')

# Save the updated file
updated_file_path = 'updatedonline_file.csv'
data.to_csv(updated_file_path, index=False)

print(f"Updated file saved as {updated_file_path}.")


```

    Updated file saved as updatedonline_file.csv.



```python


```


```python

```


---
**Score: 0**
