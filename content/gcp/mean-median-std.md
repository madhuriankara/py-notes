---
title: Mean-Median-Std
date: 2024-12-23
author: Your Name
cell_count: 5
score: 5
---

```python
#Calculate the mean, median, and standard deviation of test scores for the entire class.
```


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
def query_bigquery():
    query = """
    WITH test_scores_data AS (
    SELECT test_scores FROM `plucky-order-444214-g8.student_data.student_data_madhuri` 
    )
    SELECT
    AVG(test_scores) AS mean_score,
    APPROX_QUANTILES(test_scores, 2)[OFFSET(1)] AS median_score,
    STDDEV(test_scores) AS std_dev_score
      FROM
            test_scores_data;
    """
    result = client.query(query)
    for row in result:
        print(f"Mean Test Score: {row.mean_score}")
        print(f"Median Test Score: {row.median_score}")
        print(f"Standard Deviation of Test Scores: {row.std_dev_score}")

    
query_bigquery()
```

    Mean Test Score: 77.78999999999998
    Median Test Score: 78
    Standard Deviation of Test Scores: 11.28536640740988



```python

```


---
**Score: 5**
