---
title: Gnb
date: 2024-11-23
author: Your Name
cell_count: 4
score: 0
---

```python

from sklearn import datasets
from sklearn.naive_bayes import GaussianNB

```


```python

iris = datasets.load_iris()


gnb = GaussianNB()
y_pred = gnb.fit(iris.data, iris.target).predict(iris.data)

```


```python
print("Number of mislabeled points out of a total %d points : %d" % (iris.data.shape[0],(iris.target != y_pred).sum()))
```

    Number of mislabeled points out of a total 150 points : 6



```python

```


---
**Score: 0**
