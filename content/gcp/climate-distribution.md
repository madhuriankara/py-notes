---
title: Climate-Distribution
date: 2025-01-13
author: Your Name
cell_count: 5
score: 5
---

```python
#What is the distribution of climate types across regions?
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
def get_climate_type():
    query = """
    SELECT region,
    climate, COUNT(*) AS count,
    FROM `plucky-order-444214-g8.student_data.country_table` 
    GROUP BY region, climate;
    """
    result = client.query(query)
    print("The distribution of climate types across regions")
    for i in result:
        print(f'{i.region} -  {i.count}')

get_climate_type()
```

    The distribution of climate types across regions
    C.W. OF IND. STATES  -  2
    ASIA (EX. NEAR EAST)          -  1
    BALTICS                             -  1
    EASTERN EUROPE                      -  3
    NEAR EAST                           -  1
    NORTHERN AFRICA                     -  2
    NORTHERN AMERICA                    -  2
    SUB-SAHARAN AFRICA                  -  3
    WESTERN EUROPE                      -  7
    C.W. OF IND. STATES  -  3
    ASIA (EX. NEAR EAST)          -  4
    NEAR EAST                           -  10
    NORTHERN AFRICA                     -  3
    NORTHERN AMERICA                    -  1
    OCEANIA                             -  1
    SUB-SAHARAN AFRICA                  -  7
    C.W. OF IND. STATES  -  1
    LATIN AMER. & CARIB     -  39
    ASIA (EX. NEAR EAST)          -  18
    NORTHERN AMERICA                    -  1
    OCEANIA                             -  19
    SUB-SAHARAN AFRICA                  -  33
    C.W. OF IND. STATES  -  2
    LATIN AMER. & CARIB     -  3
    ASIA (EX. NEAR EAST)          -  3
    BALTICS                             -  2
    EASTERN EUROPE                      -  8
    NEAR EAST                           -  5
    NORTHERN AFRICA                     -  1
    NORTHERN AMERICA                    -  1
    OCEANIA                             -  1
    SUB-SAHARAN AFRICA                  -  3
    WESTERN EUROPE                      -  19
    C.W. OF IND. STATES  -  3
    EASTERN EUROPE                      -  1
    WESTERN EUROPE                      -  2
    LATIN AMER. & CARIB     -  3
    ASIA (EX. NEAR EAST)          -  1
    SUB-SAHARAN AFRICA                  -  4
    C.W. OF IND. STATES  -  1
    ASIA (EX. NEAR EAST)          -  1
    SUB-SAHARAN AFRICA                  -  1



```python

```


---
**Score: 5**
