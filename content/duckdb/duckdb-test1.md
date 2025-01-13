---
title: Duckdb-Test1
date: 2025-01-13
author: Your Name
cell_count: 10
score: 10
---

```python
!pip install duckdb
```

    Collecting duckdb
      Downloading duckdb-1.1.3-cp312-cp312-macosx_12_0_arm64.whl.metadata (762 bytes)
    Downloading duckdb-1.1.3-cp312-cp312-macosx_12_0_arm64.whl (15.5 MB)
    [2K   [38;2;114;156;31m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m15.5/15.5 MB[0m [31m34.2 MB/s[0m eta [36m0:00:00[0m31m36.0 MB/s[0m eta [36m0:00:01[0m
    [?25hInstalling collected packages: duckdb
    Successfully installed duckdb-1.1.3



```python
import duckdb
```


```python
# Connect to DuckDB
con = duckdb.connect()

```


```python
# Load CSV file
con.execute("CREATE TABLE student AS SELECT * FROM '../student_data.csv'")

```




    <duckdb.duckdb.DuckDBPyConnection at 0x104126bb0>




```python
result = con.execute("SELECT * FROM student WHERE student_id = 1").fetchall()
```


```python
result
```




    [(1, 'John Doe', 85, 90, 80, 88, 1)]




```python
import pandas as pd
from IPython.display import display

def list2table(cdata, col_list = None):

    first_row = cdata[0]
    cols_count = len(first_row)

    if not col_list:
        col_list = []
        for idx in range(cols_count):
            col_list.append(f'col_{idx}')

    # Convert the list of tuples to a DataFrame
    df1 = pd.DataFrame(cdata, columns = col_list)
    
    # Set display options
    pd.set_option('display.max_rows', 100)
    pd.set_option('display.max_columns', 100)
    
    # Apply custom styling
    styled_df = df1.style.set_properties(**{'text-align': 'center'})
    
    # Display the DataFrame
    display(styled_df)
```


```python
def q(query, col_list = None):

    result = con.execute(query).fetchall()
    # print(result)

    return list2table(result, col_list)
```


```python
q("SELECT * FROM student WHERE student_id = 1")
```


<style type="text/css">
#T_01564_row0_col0, #T_01564_row0_col1, #T_01564_row0_col2, #T_01564_row0_col3, #T_01564_row0_col4, #T_01564_row0_col5, #T_01564_row0_col6 {
  text-align: center;
}
</style>
<table id="T_01564">
  <thead>
    <tr>
      <th class="blank level0" >&nbsp;</th>
      <th id="T_01564_level0_col0" class="col_heading level0 col0" >col_0</th>
      <th id="T_01564_level0_col1" class="col_heading level0 col1" >col_1</th>
      <th id="T_01564_level0_col2" class="col_heading level0 col2" >col_2</th>
      <th id="T_01564_level0_col3" class="col_heading level0 col3" >col_3</th>
      <th id="T_01564_level0_col4" class="col_heading level0 col4" >col_4</th>
      <th id="T_01564_level0_col5" class="col_heading level0 col5" >col_5</th>
      <th id="T_01564_level0_col6" class="col_heading level0 col6" >col_6</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th id="T_01564_level0_row0" class="row_heading level0 row0" >0</th>
      <td id="T_01564_row0_col0" class="data row0 col0" >1</td>
      <td id="T_01564_row0_col1" class="data row0 col1" >John Doe</td>
      <td id="T_01564_row0_col2" class="data row0 col2" >85</td>
      <td id="T_01564_row0_col3" class="data row0 col3" >90</td>
      <td id="T_01564_row0_col4" class="data row0 col4" >80</td>
      <td id="T_01564_row0_col5" class="data row0 col5" >88</td>
      <td id="T_01564_row0_col6" class="data row0 col6" >1</td>
    </tr>
  </tbody>
</table>




```python

```


---
**Score: 10**
