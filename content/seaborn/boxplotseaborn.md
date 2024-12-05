---
title: Boxplotseaborn
date: 2024-12-05
author: Your Name
cell_count: 12
score: 10
---

```python
import pandas as pd
import matplotlib.pyplot as plt
```


```python
import seaborn as sns
```


```python
days_list = [
    1, 1, 1, 1, 1,
    2, 2, 2, 2, 2,
    3, 3, 3, 3, 3
]
```


```python
learners_list = [
    'Madhuri','Sarvana','Soundarya','Steve','Hari',
    'Madhuri','Sarvana','Soundarya','Steve','Hari',
    'Madhuri','Sarvana','Soundarya','Steve','Hari'
]
```


```python
score_list = [
    0, 0, 0, 0, 0,
    535,300,510,580,205,
    880,490,600,625,205
]
```


```python
data = {
    'days':  days_list,
    'learners': learners_list,
    'score' : score_list
}
```


```python
df = pd.DataFrame(data)
```


```python
df_wide = df.pivot(index ='days', columns = 'learners', values = 'score')
```


```python
df_wide = pd.DataFrame(data)
```


```python
sns.boxplot(data=df_wide, x="learners", y="score").set(title = "Score Distribution")

```




    [Text(0.5, 1.0, 'Score Distribution')]




    
![png](boxplotseaborn_files/boxplotseaborn_9_1.png)
    



```python

```


```python

```


---
**Score: 10**
