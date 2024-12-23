---
title: Median-5-Attendance
date: 2024-12-23
author: Your Name
cell_count: 5
score: 5
---

```python
#List students whose attendance is within 5% of the class median attendance.
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
        WITH median_attendance AS (
            SELECT 
                APPROX_QUANTILES(attendance, 2)[OFFSET(1)] AS median_attendance
            FROM 
                `plucky-order-444214-g8.student_data.student_data_madhuri`
        )
        SELECT 
            s.student_name, 
            s.attendance, 
            m.median_attendance
        FROM 
            `plucky-order-444214-g8.student_data.student_data_madhuri` AS s, 
            median_attendance AS m
        WHERE 
            ABS(s.attendance - m.median_attendance) <= 5
        ORDER BY 
            s.attendance DESC;
    """

    result = client.query(query).result()

    print("Students with attendance within 5% of the class median attendance:")
    for row in result:
        print(f"{row.student_name} - Attendance: {row.attendance}% - Median Attendance: {row.median_attendance}%")

query_bigquery()

```

    Students with attendance within 5% of the class median attendance:
    John Doe - Attendance: 90% - Median Attendance: 85%
    Alexander Torres - Attendance: 90% - Median Attendance: 85%
    Steven Green - Attendance: 90% - Median Attendance: 85%
    Jeffrey Hughes - Attendance: 90% - Median Attendance: 85%
    Kevin Young - Attendance: 89% - Median Attendance: 85%
    Frank Morgan - Attendance: 89% - Median Attendance: 85%
    Frank Palmer - Attendance: 89% - Median Attendance: 85%
    Daniel Lewis - Attendance: 88% - Median Attendance: 85%
    Brian Edwards - Attendance: 88% - Median Attendance: 85%
    Kenneth Butler - Attendance: 88% - Median Attendance: 85%
    David Anderson - Attendance: 87% - Median Attendance: 85%
    Justin Bennett - Attendance: 87% - Median Attendance: 85%
    Ronald Lee - Attendance: 87% - Median Attendance: 85%
    Paul Mitchell - Attendance: 86% - Median Attendance: 85%
    Jane Smith - Attendance: 85% - Median Attendance: 85%
    Sandra Turner - Attendance: 81% - Median Attendance: 85%
    Alice Brown - Attendance: 80% - Median Attendance: 85%
    Sarah Taylor - Attendance: 80% - Median Attendance: 85%
    Sharon Cook - Attendance: 80% - Median Attendance: 85%



```python

```


---
**Score: 5**
