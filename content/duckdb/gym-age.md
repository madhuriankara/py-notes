---
title: Gym-Age
date: 2025-01-22
author: Your Name
cell_count: 6
score: 5
---

```python
import duckdb
```


```python
con = duckdb.connect()
```


```python
con.execute("CREATE TABLE gym AS SELECT * FROM 'gym.csv'")
```




    <duckdb.duckdb.DuckDBPyConnection at 0x1180eb530>




```python
result = con.execute("""SELECT age FROM gym
                        WHERE Gender == 'Male' """).fetchall()
```


```python
result
```




    [(56,),
     (25,),
     (38,),
     (36,),
     (28,),
     (28,),
     (41,),
     (53,),
     (57,),
     (41,),
     (20,),
     (19,),
     (38,),
     (29,),
     (44,),
     (59,),
     (45,),
     (32,),
     (38,),
     (26,),
     (35,),
     (21,),
     (42,),
     (43,),
     (37,),
     (45,),
     (24,),
     (25,),
     (53,),
     (57,),
     (21,),
     (23,),
     (27,),
     (53,),
     (32,),
     (40,),
     (35,),
     (41,),
     (43,),
     (46,),
     (41,),
     (25,),
     (28,),
     (25,),
     (52,),
     (22,),
     (56,),
     (58,),
     (26,),
     (29,),
     (51,),
     (50,),
     (41,),
     (54,),
     (52,),
     (18,),
     (52,),
     (54,),
     (20,),
     (18,),
     (43,),
     (31,),
     (56,),
     (44,),
     (26,),
     (32,),
     (59,),
     (30,),
     (56,),
     (49,),
     (21,),
     (54,),
     (56,),
     (53,),
     (49,),
     (39,),
     (45,),
     (59,),
     (23,),
     (45,),
     (37,),
     (45,),
     (42,),
     (18,),
     (30,),
     (58,),
     (20,),
     (56,),
     (23,),
     (50,),
     (59,),
     (41,),
     (32,),
     (49,),
     (41,),
     (20,),
     (54,),
     (19,),
     (19,),
     (45,),
     (54,),
     (50,),
     (18,),
     (36,),
     (43,),
     (21,),
     (28,),
     (34,),
     (55,),
     (23,),
     (28,),
     (50,),
     (26,),
     (37,),
     (20,),
     (36,),
     (49,),
     (58,),
     (50,),
     (57,),
     (56,),
     (28,),
     (48,),
     (47,),
     (59,),
     (43,),
     (19,),
     (29,),
     (22,),
     (54,),
     (49,),
     (58,),
     (52,),
     (36,),
     (33,),
     (41,),
     (50,),
     (41,),
     (28,),
     (25,),
     (53,),
     (57,),
     (42,),
     (52,),
     (50,),
     (50,),
     (38,),
     (37,),
     (20,),
     (50,),
     (29,),
     (39,),
     (39,),
     (47,),
     (55,),
     (25,),
     (44,),
     (50,),
     (45,),
     (50,),
     (36,),
     (52,),
     (45,),
     (47,),
     (46,),
     (58,),
     (54,),
     (52,),
     (38,),
     (40,),
     (48,),
     (49,),
     (40,),
     (59,),
     (43,),
     (34,),
     (50,),
     (46,),
     (59,),
     (43,),
     (52,),
     (30,),
     (25,),
     (33,),
     (29,),
     (40,),
     (32,),
     (49,),
     (42,),
     (59,),
     (23,),
     (32,),
     (22,),
     (56,),
     (49,),
     (47,),
     (52,),
     (57,),
     (30,),
     (34,),
     (36,),
     (45,),
     (43,),
     (43,),
     (40,),
     (29,),
     (56,),
     (22,),
     (39,),
     (46,),
     (29,),
     (33,),
     (54,),
     (39,),
     (31,),
     (47,),
     (22,),
     (29,),
     (43,),
     (56,),
     (53,),
     (40,),
     (22,),
     (48,),
     (36,),
     (49,),
     (22,),
     (21,),
     (41,),
     (33,),
     (19,),
     (49,),
     (41,),
     (29,),
     (52,),
     (50,),
     (54,),
     (29,),
     (20,),
     (18,),
     (27,),
     (46,),
     (30,),
     (29,),
     (19,),
     (34,),
     (27,),
     (43,),
     (58,),
     (24,),
     (21,),
     (28,),
     (46,),
     (42,),
     (38,),
     (53,),
     (27,),
     (52,),
     (35,),
     (56,),
     (49,),
     (41,),
     (40,),
     (40,),
     (52,),
     (47,),
     (34,),
     (42,),
     (39,),
     (36,),
     (36,),
     (29,),
     (26,),
     (45,),
     (36,),
     (22,),
     (52,),
     (29,),
     (42,),
     (38,),
     (56,),
     (59,),
     (56,),
     (48,),
     (40,),
     (46,),
     (35,),
     (26,),
     (27,),
     (55,),
     (30,),
     (26,),
     (19,),
     (22,),
     (46,),
     (36,),
     (25,),
     (39,),
     (34,),
     (42,),
     (53,),
     (48,),
     (36,),
     (44,),
     (43,),
     (45,),
     (37,),
     (56,),
     (18,),
     (20,),
     (30,),
     (55,),
     (23,),
     (49,),
     (38,),
     (54,),
     (53,),
     (36,),
     (35,),
     (48,),
     (18,),
     (40,),
     (28,),
     (29,),
     (49,),
     (33,),
     (55,),
     (29,),
     (41,),
     (45,),
     (54,),
     (53,),
     (44,),
     (26,),
     (50,),
     (37,),
     (30,),
     (45,),
     (23,),
     (22,),
     (42,),
     (19,),
     (27,),
     (50,),
     (35,),
     (38,),
     (42,),
     (44,),
     (30,),
     (58,),
     (38,),
     (23,),
     (34,),
     (22,),
     (48,),
     (20,),
     (54,),
     (27,),
     (27,),
     (34,),
     (26,),
     (18,),
     (21,),
     (18,),
     (57,),
     (49,),
     (51,),
     (25,),
     (56,),
     (43,),
     (20,),
     (47,),
     (34,),
     (32,),
     (38,),
     (19,),
     (28,),
     (56,),
     (55,),
     (51,),
     (47,),
     (32,),
     (51,),
     (55,),
     (41,),
     (32,),
     (47,),
     (59,),
     (21,),
     (27,),
     (27,),
     (34,),
     (37,),
     (41,),
     (19,),
     (40,),
     (33,),
     (21,),
     (42,),
     (49,),
     (20,),
     (44,),
     (36,),
     (35,),
     (45,),
     (39,),
     (58,),
     (29,),
     (43,),
     (51,),
     (44,),
     (47,),
     (34,),
     (43,),
     (18,),
     (25,),
     (52,),
     (32,),
     (39,),
     (31,),
     (40,),
     (31,),
     (43,),
     (31,),
     (24,),
     (20,),
     (35,),
     (55,),
     (52,),
     (32,),
     (27,),
     (56,),
     (56,),
     (39,),
     (37,),
     (42,),
     (27,),
     (35,),
     (39,),
     (51,),
     (25,),
     (57,),
     (59,),
     (51,),
     (23,),
     (39,),
     (23,),
     (21,),
     (47,),
     (26,),
     (48,),
     (57,),
     (45,),
     (21,),
     (47,),
     (32,),
     (22,),
     (37,),
     (50,),
     (18,),
     (43,),
     (55,),
     (28,),
     (53,),
     (30,),
     (20,),
     (23,),
     (27,),
     (40,),
     (27,),
     (30,),
     (54,),
     (34,),
     (26,),
     (28,),
     (32,),
     (41,),
     (55,),
     (52,),
     (47,),
     (48,),
     (22,),
     (51,),
     (18,),
     (57,),
     (39,),
     (46,),
     (31,),
     (47,),
     (52,),
     (54,),
     (22,),
     (43,),
     (21,),
     (42,),
     (59,),
     (42,),
     (35,),
     (57,),
     (49,),
     (55,),
     (40,),
     (32,),
     (50,),
     (57,),
     (23,),
     (20,),
     (24,),
     (25,),
     (32,),
     (46,)]




```python

```


---
**Score: 5**
