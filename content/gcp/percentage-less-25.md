---
title: Percentage-Less-25
date: 2024-12-23
author: Your Name
cell_count: 6
score: 5
---

```python
#Find students whose test scores are in the bottom 25% of the class.
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
    SELECT student_name, test_scores, COUNT(*) AS percentage_students FROM `plucky-order-444214-g8.student_data.student_data_madhuri`
    WHERE test_scores <= 25
    GROUP BY student_name
"""

    result = client.query(query)
    print("Number of students who scored below 25%:")
    for row in result:
        print(f"{row.student_name} - {row.test_scores}")
```


```python
query_bigquery()
```

    Number of students who scored below 25%:



    ---------------------------------------------------------------------------

    BadRequest                                Traceback (most recent call last)

    Cell In[31], line 1
    ----> 1 query_bigquery()


    Cell In[30], line 10, in query_bigquery()
          8 result = client.query(query)
          9 print("Number of students who scored below 25%:")
    ---> 10 for row in result:
         11     print(f"{row.student_name} - {row.test_scores}")


    File /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/cloud/bigquery/job/query.py:2164, in QueryJob.__iter__(self)
       2163 def __iter__(self):
    -> 2164     return iter(self.result())


    File /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/cloud/bigquery/job/query.py:1681, in QueryJob.result(self, page_size, max_results, retry, timeout, start_index, job_retry)
       1676     remaining_timeout = None
       1678 if remaining_timeout is None:
       1679     # Since is_job_done() calls jobs.getQueryResults, which is a
       1680     # long-running API, don't delay the next request at all.
    -> 1681     while not is_job_done():
       1682         pass
       1683 else:
       1684     # Use a monotonic clock since we don't actually care about
       1685     # daylight savings or similar, just the elapsed time.


    File /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/api_core/retry/retry_unary.py:293, in Retry.__call__.<locals>.retry_wrapped_func(*args, **kwargs)
        289 target = functools.partial(func, *args, **kwargs)
        290 sleep_generator = exponential_sleep_generator(
        291     self._initial, self._maximum, multiplier=self._multiplier
        292 )
    --> 293 return retry_target(
        294     target,
        295     self._predicate,
        296     sleep_generator,
        297     timeout=self._timeout,
        298     on_error=on_error,
        299 )


    File /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/api_core/retry/retry_unary.py:153, in retry_target(target, predicate, sleep_generator, timeout, on_error, exception_factory, **kwargs)
        149 # pylint: disable=broad-except
        150 # This function explicitly must deal with broad exceptions.
        151 except Exception as exc:
        152     # defer to shared logic for handling errors
    --> 153     _retry_error_helper(
        154         exc,
        155         deadline,
        156         sleep,
        157         error_list,
        158         predicate,
        159         on_error,
        160         exception_factory,
        161         timeout,
        162     )
        163     # if exception not raised, sleep before next attempt
        164     time.sleep(sleep)


    File /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/api_core/retry/retry_base.py:212, in _retry_error_helper(exc, deadline, next_sleep, error_list, predicate_fn, on_error_fn, exc_factory_fn, original_timeout)
        206 if not predicate_fn(exc):
        207     final_exc, source_exc = exc_factory_fn(
        208         error_list,
        209         RetryFailureReason.NON_RETRYABLE_ERROR,
        210         original_timeout,
        211     )
    --> 212     raise final_exc from source_exc
        213 if on_error_fn is not None:
        214     on_error_fn(exc)


    File /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/api_core/retry/retry_unary.py:144, in retry_target(target, predicate, sleep_generator, timeout, on_error, exception_factory, **kwargs)
        142 for sleep in sleep_generator:
        143     try:
    --> 144         result = target()
        145         if inspect.isawaitable(result):
        146             warnings.warn(_ASYNC_RETRY_WARNING)


    File /opt/homebrew/Caskroom/miniconda/base/envs/py312/lib/python3.12/site-packages/google/cloud/bigquery/job/query.py:1630, in QueryJob.result.<locals>.is_job_done()
       1607 if job_failed_exception is not None:
       1608     # Only try to restart the query job if the job failed for
       1609     # a retriable reason. For example, don't restart the query
       (...)
       1627     # into an exception that can be processed by the
       1628     # `job_retry` predicate.
       1629     restart_query_job = True
    -> 1630     raise job_failed_exception
       1631 else:
       1632     # Make sure that the _query_results are cached so we
       1633     # can return a complete RowIterator.
       (...)
       1639     # making any extra API calls if the previous loop
       1640     # iteration fetched the finished job.
       1641     self._reload_query_results(
       1642         retry=retry, **reload_query_results_kwargs
       1643     )


    BadRequest: 400 SELECT list expression references column test_scores which is neither grouped nor aggregated at [2:26]; reason: invalidQuery, location: query, message: SELECT list expression references column test_scores which is neither grouped nor aggregated at [2:26]
    
    Location: northamerica-northeast2
    Job ID: 5e235067-736b-49ad-be88-7cd2f92861e0




```python

```


---
**Score: 5**
