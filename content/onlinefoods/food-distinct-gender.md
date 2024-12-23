---
title: Food-Distinct-Gender
date: 2024-12-23
author: Your Name
cell_count: 9
score: 5
---

```python
from google.cloud import bigquery
```


```python
client = bigquery.Client()
```

    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)
    /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/auth/_default.py:76: UserWarning: Your application has authenticated using end user credentials from Google Cloud SDK without a quota project. You might receive a "quota exceeded" or "API not enabled" error. See the following page for troubleshooting: https://cloud.google.com/docs/authentication/adc-troubleshooting/user-creds. 
      warnings.warn(_CLOUD_SDK_CREDENTIALS_WARNING)



```python
import pandas as pd
```


```python
FILEPATH = '/Users/madhuriankaraboyina/Downloads/onlinefoods.csv'
```


```python
df = pd.read_csv(FILEPATH)
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Gender</th>
      <th>Marital Status</th>
      <th>Occupation</th>
      <th>Monthly Income</th>
      <th>Educational Qualifications</th>
      <th>Family size</th>
      <th>latitude</th>
      <th>longitude</th>
      <th>Pin code</th>
      <th>Output</th>
      <th>Feedback</th>
      <th>Unnamed: 12</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>20</td>
      <td>Female</td>
      <td>Single</td>
      <td>Student</td>
      <td>No Income</td>
      <td>Post Graduate</td>
      <td>4</td>
      <td>12.9766</td>
      <td>77.5993</td>
      <td>560001</td>
      <td>Yes</td>
      <td>Positive</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>1</th>
      <td>24</td>
      <td>Female</td>
      <td>Single</td>
      <td>Student</td>
      <td>Below Rs.10000</td>
      <td>Graduate</td>
      <td>3</td>
      <td>12.9770</td>
      <td>77.5773</td>
      <td>560009</td>
      <td>Yes</td>
      <td>Positive</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>2</th>
      <td>22</td>
      <td>Male</td>
      <td>Single</td>
      <td>Student</td>
      <td>Below Rs.10000</td>
      <td>Post Graduate</td>
      <td>3</td>
      <td>12.9551</td>
      <td>77.6593</td>
      <td>560017</td>
      <td>Yes</td>
      <td>Negative</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>3</th>
      <td>22</td>
      <td>Female</td>
      <td>Single</td>
      <td>Student</td>
      <td>No Income</td>
      <td>Graduate</td>
      <td>6</td>
      <td>12.9473</td>
      <td>77.5616</td>
      <td>560019</td>
      <td>Yes</td>
      <td>Positive</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>4</th>
      <td>22</td>
      <td>Male</td>
      <td>Single</td>
      <td>Student</td>
      <td>Below Rs.10000</td>
      <td>Post Graduate</td>
      <td>4</td>
      <td>12.9850</td>
      <td>77.5533</td>
      <td>560010</td>
      <td>Yes</td>
      <td>Positive</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>383</th>
      <td>23</td>
      <td>Female</td>
      <td>Single</td>
      <td>Student</td>
      <td>No Income</td>
      <td>Post Graduate</td>
      <td>2</td>
      <td>12.9766</td>
      <td>77.5993</td>
      <td>560001</td>
      <td>Yes</td>
      <td>Positive</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>384</th>
      <td>23</td>
      <td>Female</td>
      <td>Single</td>
      <td>Student</td>
      <td>No Income</td>
      <td>Post Graduate</td>
      <td>4</td>
      <td>12.9854</td>
      <td>77.7081</td>
      <td>560048</td>
      <td>Yes</td>
      <td>Positive</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>385</th>
      <td>22</td>
      <td>Female</td>
      <td>Single</td>
      <td>Student</td>
      <td>No Income</td>
      <td>Post Graduate</td>
      <td>5</td>
      <td>12.9850</td>
      <td>77.5533</td>
      <td>560010</td>
      <td>Yes</td>
      <td>Positive</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>386</th>
      <td>23</td>
      <td>Male</td>
      <td>Single</td>
      <td>Student</td>
      <td>Below Rs.10000</td>
      <td>Post Graduate</td>
      <td>2</td>
      <td>12.9770</td>
      <td>77.5773</td>
      <td>560009</td>
      <td>Yes</td>
      <td>Positive</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>387</th>
      <td>23</td>
      <td>Male</td>
      <td>Single</td>
      <td>Student</td>
      <td>No Income</td>
      <td>Post Graduate</td>
      <td>5</td>
      <td>12.8988</td>
      <td>77.5764</td>
      <td>560078</td>
      <td>Yes</td>
      <td>Positive</td>
      <td>Yes</td>
    </tr>
  </tbody>
</table>
<p>388 rows × 13 columns</p>
</div>




```python
#What are the distinct values present in the Gender column
```


```python
def get_distint_gender():
    query = """
    SELECT DISTINCT Gender FROM `plucky-order-444214-g8.student_data.online_food`
    """
    result = client.query(query)
    print("The gender is now displayed")
    for i in result:
        print(f'{i.Gender}')
get_distint_gender()
```

    The gender is now displayed
    Male
    Female



```python

```


---
**Score: 5**
